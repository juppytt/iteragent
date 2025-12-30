# vibe-analyzer

Analyze multiple input files for the same task using Claude, Codex, and Gemini, rotating on rate limits.

## Usage
Provide input directory and prompt with a `{{INPUT_FILE}}` placeholder. `inputs/` and `SAMPLE_TASK.md` are samples.

```bash
python run.py <input_dir> --prompts <prompt_file>
```

## Args
- `input_dir`: directory of input files (default: `inputs`)
- `--prompts`: prompt template file (default: `TASK.md`)
- `--output-dir`: output directory (default: `runs`)
- `--sample-run`: run only the first input file
