# Claude Code Project Checklist

## Getting Set Up

- Be specific in your prompt about app features, tech stack, external resources, etc.
- Ask Claude to begin with minimal graphical design and focus mainly on functionality
- Claude should put sensitive information in a `.env` or a `.env.local` file and add them to a `.gitignore`
- Start in plan mode... having Claude get it right the first time will save effort later
- Claude should write a CLAUDE.md with details about the project and stack so additional sessions immediately know what you've built
- Ask Claude to commit and push your repo to GitHub

## For Each New Feature

- Ask Claude to begin that new feature on a git branch
- Be specific in your prompt and also the files to work in if you can to limit the scope of Claude's work
- Be sure to test after you build as well as build automated tests for the feature once it's complete
- Once the feature is complete, have Claude create and merge a PR for you
- Delete the branch once the merge is complete so you can keep your workspace clean

## Testing

- Ask Claude to build tests for your project
- It's better to ask Claude to build tests for individual pieces you're aware of... for example if you have a backend API and a frontend interface, ask Claude in individual sessions to build tests for each
- Set up GitHub actions so your tests run with every commit
- Alternately you may set up a Claude hook to run every time you commit

## Security

- Ask Claude to run a security audit using the OWASP top ten list
- Security should be robust so use a high grade model and optionally break the audit into subagents using one agent for each security concern
- Also use a high grade model to set up a red team hacker to attempt to find security vulnerabilities as well
- Have Claude set up security logging which alerts you to potential hacks and break ins
- Each of these should be their own session to avoid context leaking and influencing other parts of your "security team"

## Design

- Build design components with Claude Design and incorporate them
- Ask Claude to apply your design to your application
- Use the design components for any new features and optionally iterate and expand on the design as necessary

## Deployment

- Claude will generally have a good workflow with deployment and might be able to run deployment for you
- You should manually move sensitive information from a `.env` file to the deployed environment
- Have friends test your app! The less they know about it beforehand the better feedback they can give!
