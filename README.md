# Writing Style Prompt Challenges (Sonnet)
I am having trouble getting Sonnet to follow writing style instructions. 
The writing style varies considerably depending on whether ```claude-3-5-sonnet-20240620``` or ```claude-3-5-sonnet-20241022``` is used, with the older Sonnet doing a much better job of following the writing style instructions.

To write consistently in a specific format and make it token-efficient, I am using a strategy where I provide a JSON object that describes a writing style in detail. This has worked well in previous versions of Sonnet.

The new Sonnet writes with vocabulary and sentence structure that is too advanced. Since I am creating YouTube scripts, the writing needs to be very simple and conversational.

## Frame Prompt
The goal of this prompt is to describe the unique angle and audience goals for a YouTube script we're in the process of writing.

I have developed an elaborate writing style description in JSON format that I've been using successfully with the older Sonnet.

I've been trying to use the same writing style description with the new Sonnet, but it is not working as well.

See [frame-production.md](frame-production.md) for the production prompt with detailed writing style description.

I've tried to simplify the writing style description, but it is not working well either.

See [frame-simple.md](frame-simple.md) for the simple prompt with simplified writing style description.

## Testing Methodology
1. Open Workbench and paste the system prompt and user prompt from each example
2. Select Sonnet 20240620 with Temp 1 and observe the JSON values to look for the writing style described by the last few lines of the user prompt. Confirm that it is being followed.
3. Select Sonnet 20241022 with Temp 1 and observe the JSON values to look for the writing style described by the last few lines of the user prompt. Observe that it is not being followed.
## Other things I've tried:
- Moving the writing style description to a separate message pair, with the AI responding to the first user prompt and asking whether a certain style should be used.
- Using the writing style description as a system prompt.
- Converting the JSON description of the writing style to more of a narrative description in paragraph format.
- Passing in blocks of text that describe the writing style vs using a JSON-based style.
