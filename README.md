# 🌍 Fine-Tuning LLM for Geospatial Raster & Vector Data | BISAG-N Internship Project

This project explores how to fine-tune a large language model (LLM) using geospatial raster and vector datasets. Conducted as part of a summer internship at **BISAG-N (Bhaskaracharya National Institute for Space Applications & Geo-informatics)**, the goal was to train the model to understand natural language queries and output appropriate GDAL (Geospatial Data Abstraction Library) commands.

---

## 📌 Project Highlights

- 🔁 **Fine-tuned** [Zephyr-7B-Beta](https://huggingface.co/HuggingFaceH4/zephyr-7b-beta) using **LoRA** (Low-Rank Adaptation)
- 🌐 Trained the model to map **natural language queries to GDAL CLI commands**
- 💻 Built an interactive **Gradio UI** for querying the model
- 🛰️ Focused on real-world **raster (.tif)** and **vector (.shp)** geospatial data
- 🧠 Performed model training using **QLoRA** on Google Colab Free Tier

---

## 🏢 Internship Organization: BISAG-N

BISAG-N is a premier institution under the **Ministry of Electronics and Information Technology, Government of India**, focused on leveraging space and geospatial technology for governance, sustainability, and development.

---

## 🧠 Technologies Used

| Category | Tools |
|---------|-------|
| Language Model | Zephyr-7B-Beta, TinyLLaMA |
| Fine-tuning | PEFT (LoRA, QLoRA), Transformers, PyTorch |
| Geospatial | GDAL, GeoPandas, QGIS |
| UI | Gradio |
| Platform | Google Colab |
| Data Format | JSONL for prompt-response pairs |

---

## 📂 Dataset

- Over **5000** prompt–response pairs provided by BISAG-N
- Each pair mapped a natural language geospatial task to a GDAL command
- Example:

```json
{
  "instruction": "Clip raster to boundary",
  "response": "gdalwarp -cutline boundary.shp -crop_to_cutline input.tif output.tif"
}
