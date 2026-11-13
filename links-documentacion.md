Docs about GitHub Agentic Workflows
https://docs.github.com/en/copilot/concepts/agent-capabilities/agent-powered-workflows-and-operations/about-github-agentic-workflows

Ejemplo de creación de un workflow agente
```
Generate a workflow that creates a daily repo status report for a maintainer. Use the instructions at https://github.com/github/gh-aw/blob/main/create.md
```

Instalar y compilar un agent workflow
```
gh extension install github/gh-aw
gh aw compile
```

Ejecutar un agent workflow
```
gh aw run YOUR-WORKFLOW-NAME
```