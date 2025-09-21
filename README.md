# 🧾 AI Brochure Generator

An AI-powered brochure generator built in **JupyterLab** that automatically creates a company brochure for prospective clients, investors, and potential recruits.  
It scrapes content from a company’s primary website and relevant internal pages, then uses a **local LLaMA model** to generate a structured brochure in **Markdown** format.

---

## 🚀 Business Challenge
- Build a product that generates a professional brochure for a company.  
- Input: Company name and primary website URL.  
- Output: Brochure containing company culture, customers, products, and careers/jobs information.

---

## 🛠️ Features
- 🌐 **Web scraping** of main website and related internal pages using `requests` + `BeautifulSoup`.  
- 🔗 **Link analysis**: Automatically selects relevant links (About, Careers, Company pages) for brochure content.  
- 🦙 **Local LLaMA model**: Generates brochure content in Markdown format.  
- 📄 **Markdown output**: Easy to read and shareable brochure.

---


🧪 Usage
Open JupyterLab:

bash
Copy code
jupyter lab
Open notebooks/brochure_generator.ipynb.

Enter a company name and website URL in the provided cells.

The notebook will:

Scrape the landing page and internal pages for relevant content.

Analyze links and select pages relevant to a brochure (About, Careers, etc.).

Generate a short brochure in Markdown using the local LLaMA model.

Display the brochure in the notebook using Markdown:

python
Copy code
create_brochure("Company Name", "https://companywebsite.com")
Optionally, stream the brochure content live:

python
Copy code
stream_brochure("Company Name", "https://companywebsite.com")


📌 Example Workflow
Input: "HuggingFace", "https://huggingface.co"

Process:

Scrapes landing page + relevant internal links

Extracts content (company info, careers, products)

Generates Markdown brochure via local LLaMA

Output: A short brochure containing company description, culture, and opportunities.

⚡ Notes

Ensure your local LLaMA instance is running and accessible at http://localhost:11434.

Some websites require headers to avoid being blocked; headers are included in the Website class.

Emails, Terms of Service, and Privacy links are filtered out automatically.
