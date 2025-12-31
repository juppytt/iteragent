# iteragent

Analyze multiple input files for the same task using Claude, Codex, and Gemini, rotating on failures.

## Usage
Provide input directory and task with a `{{INPUT_FILE}}` placeholder. Samples live in `sample_summarize/input` and `sample_summarize/TASK.md`, plus `sample_web/input` and `sample_web/TASK.md`.

```bash
python run.py <input_dir> --task <task_file>
```

## Args
- `input_dir`: directory of input files, or a single input file (default: `input`)
- `--task`: prompt template file (default: `TASK.md`)
- `--output-dir`: output directory (default: `output`)
- `--sample-run`: run only the first input file
- `--force-rerun`: rerun even if output already exists
- `--bwrap`: run agents with bubblewrap (input read-only, output writable)
- `--agents`: comma-separated agent list (default: `claude,codex,gemini`)
