# Functional UI with Stageshow

The user chose Stageshow for its visual results. Use it rather than substituting another design system or running a second design workflow.

Read the installed Stageshow skill and select a relevant example/reference for hierarchy, typography, spacing, palette, and component treatment. The user's contest preferences scope it to a real working product: preserve usable controls, real data, complete workflows, and visible failure states. A demonstration kit or authored scene is not evidence of application functionality.

Use the application's components for actual interaction. Stageshow does not require shadcn/ui; use shadcn only when it fits the stack and reduces work. Do not add fake browser chrome, marketing sections, placeholder statistics, or staged interactions unless the brief requires them. Limit ornamental animation. Verify the rendered application with representative real data and error/empty states.

## Korean product copy

- Headings, navigation, columns, and compact status labels can use clear nouns: `운영 현황`, `검증 결과`, `처리 내역`.
- Buttons describe the actual action: `결과 보기`, `다시 계산`, `저장`.
- Use consistent, natural explanatory Korean. Keep domain terms stable; avoid replacing precise terms with vague friendly phrases.
- Avoid slogans and decorative subtitles in task screens. `모든 여정을, 한눈에` does not identify a screen's function.
- Errors state the observed problem, effect, and a supported next step. Do not guarantee retry success or invent notifications, saved data, or other behavior.
- Preserve amounts, dates, conditions, actors, and uncertainty during rewrites. Do not hide hard restrictions behind positive wording.
- Use 해요체 for explanatory messages where appropriate; do not turn every noun label into a conversational sentence.

These project preferences draw on [Toss's writing principles](https://toss.tech/article/8-writing-principles-of-toss) and the [Apps in Toss UX writing guide](https://developers-apps-in-toss.toss.im/design/consumer-ux-guide). They do not require an Apps in Toss application or unrelated branding/submission rules.
