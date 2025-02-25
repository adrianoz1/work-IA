## Automations to Make Daily Work Easier with AI

Personal repository with automations, prompts, agents, and other AI resources to make my daily work as a programmer easier.

## Installing podman and lobechat

To create, manage, and use the agents available here, Lobechat was used: https://lobechat.com/

Lobechat is an open-source LLMs UI compatible with the main AI models in the market such as OpenAI ChatGPT, Claude, Gemini, Groq, and Ollama.

To run Lobechat, Podman was used: https://github.com/containers/podman Podman is a tool for managing containers and images, volumes mounted within those containers, and pods made up of groups of containers.


## Running lobechat on podman
```
docker run -d -p 3210:3210 \
  --name lobe-chat \
  lobehub/lobe-chat

running on http://localhost:3210/chat
```

## Generate git diff
How to generate the change file to provide to the agents so they can generate the texts according to the changes made.

```
git checkout main && git pull origin main
git checkout fix/APAWEC-5470 && git merge main
git diff main..fix/APAWEC-5470 > diff_output.diff
```

## My personal agents
- [Master Bug](agents/master-bug.md): Hello, I'm Master Bug, cause bug description generator. Let's start chatting!
- [Master PR's](agents/master-pr.md): Hello, I'm Master PR's, Pull Request description generator. Let's start chatting!
- [Code Reviewer](agents/code-reviewer.md): Hello, I'm Code Reviewer, Check if everything has been implemented according to the task criteria. Let's start chatting!
- [GMUD Writer](agents/gmud.md): Hi, I'm (writer) GMUDs, Help write the GMUD based on the pr description, let's talk!
