# Resume building from markdown

## Tools required
- Pandoc
- wkhtmtopdf

## Workflow
- Use pandoc to convert .md to .html, with styling via a .css file
- Use wkhtmltopdf to print .html as .pdf
- Use pandoc to convert .md to .docx with styling via a .docx reference file

```sh
git clone https://github.com/sriram-yeluri/resume.git
cd resume
pandoc -o resume.html -c resume-css-stylesheet.css resume.md
wkhtmltopdf resume.html resume.pdf 
pandoc -o resume.docx --reference-docx=resume-docx-reference.docx resume.md
```

