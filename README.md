# How India Uses AI: What Skills Should Indian Professionals Focus On?

I wanted to know what people in India actually use AI for, and how that compares
with other countries. So I analysed real AI usage data from the Anthropic Economic
Index, comparing India with the US and Brazil.

**Full notebook on Kaggle:**
[What AI Skills Should India Train For](https://www.kaggle.com/code/tishasharma1/what-ai-skills-should-india-train-for)

## Key findings
- **India is the world's second-biggest user of Claude.ai**, with about 7% of all
  conversations, behind only the US.
- **Almost half of India's AI use is coding.** Coding and app-building make up about
  45% of Indian usage, much more than in the US or Brazil.
- **The same 10 coding tasks take up 38% of India's AI use**, compared with 20% in
  Brazil and 15% in the US.
- **Outside of coding, India looks a lot like the US.** When Indian users use AI for
  writing, studying or research, the mix is very similar to Americans.
- **Indian users learn with AI less.** About 14% of Indian conversations are about
  understanding something, compared with 21% in the US.

**In short:** India's AI use isn't weak, it's narrow.

![Almost half of India's AI use is coding](chart-coding-share.png)

![The same coding tasks take up far more of India's AI use](chart-country-comparison.png)

![How Indian users work with AI](chart-collaboration.png)

## Interesting problems I ran into
- **Namibia went missing.** Its country code is "NA", which pandas reads as missing
  data by default. The file was fine; the tool misread it.
- **India and Indiana share a code.** "IN" means India in country rows but Indiana in
  US-state rows, so I always filtered by geography too.
- **Percentages can mislead.** Each country's usage adds up to 100%, so India's huge
  coding share made everything else look small. I removed coding and rescaled the
  rest, and the apparent gaps in writing and research mostly disappeared.

## Tools
Python, pandas, matplotlib, Kaggle Notebooks

## Data
[Anthropic Economic Index](https://huggingface.co/datasets/Anthropic/EconomicIndex),
September 2025 release, licensed under CC-BY 4.0. It covers one week of Claude.ai
conversations (August 4 to 11, 2025), broken down by country and task.

## Limitations
This only covers Claude users over one week, so it's a snapshot rather than the full
picture of AI use in India. It shows how people use AI, not what they need or what
employers want.
