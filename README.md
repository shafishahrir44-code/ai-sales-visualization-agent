# AI Sales Visualization Agent

An interactive notebook that uses the Qwen2.5-0.5B-Instruct language model to generate pandas and Matplotlib charts from natural-language requests about the included sales dataset.

## Project files

- `ai_sales_visualization_agent.ipynb` — model setup, interactive chart prompts, and example visualization requests.
- `sales.csv` — input dataset (3,200 records).
- `requirements.txt` — Python dependencies.

## Run the notebook

1. Create and activate a Python environment.
2. Install dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

3. Launch Jupyter from this directory and open `ai_sales_visualization_agent.ipynb`:

   ```bash
   jupyter notebook
   ```

4. Run the setup cell. It loads `Qwen/Qwen2.5-0.5B-Instruct` through Hugging Face Transformers and reads `sales.csv` from the current directory. The model files are downloaded on first use. Enter a chart request in the notebook prompt and type `exit` to stop.

A CUDA-enabled GPU can be used when available; otherwise the notebook loads the model on CPU, which may be slower.

## Example requests

- Total profit per year as a bar chart
- Profit by region as a bar chart
- Profit share by category as a pie chart

## Dataset

The CSV includes date and calendar fields, geography, product and category, sales channel and customer segment, units, pricing and discount, gross and net sales, cost, returns, marketing spend, profit, campaign, and promotion status.

## Generated code

The notebook executes model-generated Python using `exec`. Generated code runs with the notebook process's local permissions. Review generated code before execution when using data or a machine that requires tighter controls.
