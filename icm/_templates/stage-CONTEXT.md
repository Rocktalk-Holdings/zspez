# {NN}_{stage-name} — {the job in five words}

One job: {the single thing this stage does}.

## Inputs

- Working (this run): ../{prev-stage-folder}/output/{file}
- Reference (every run): ../../_shared/{rules-file}.md

Do NOT load: {what an eager agent would wrongly pull in}.

## Process

1. {Read the inputs.}
2. {Transform, following the reference constraints.}
3. {Hard limits: length, count, format.}

## Outputs

- {artifact}.md → output/

## Human check

{One concrete act. Edit the output in place — the next stage reads whatever is here.}
