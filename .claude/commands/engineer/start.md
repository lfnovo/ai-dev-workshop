
# Engineer Start

This is the command to trigger the start of development for a feature.

## Setup
- If we are not in a feature branch, ask for permission to create one
- If we are in a feature branch that matches the feature name, we are good. 
- Make sure there is a .claude/sessions/<feature_slug> folder
- Ask the user for the input for this session (you will be given one or more linear cards to work on)

## Analysis

Go through the cards, parents and children if required, and build an initial understanding of what needs to be build. Think carefully about what is requested, ensure you understand exactly: 
    - Why this is being built (context)
    - What is the expected outcome for this issue? (goal)
    - How should it be built, just directionally, not in details (approach)
    - If it requires using new APIs/tools, do you understand them?
    - How should this be tested?
    - What are the dependencies?
    - What are the constraints?

After you reflect on this questions, come up with the 3-5 most important clarifications needed to complete the task. Ask the human for those questions, while also providing your understanding and suggestions.

After you get the human's answers, ponder on whether you need to ask more questions. If so, ask the human more questions.

Once you have a good understanding of what is being built, save it in the .claude/sessions/<feature_slug>/context.md file and ask the human to review it.

If the human agrees with your understanding, you can proceed to the next step. Otherwise, keep iterating together until you get explicit approval to  move forward.

If anything you discussed here affects what has been written in the requirements, ask the human for permission to edit those requirements and make adjustments either by editing (structural changes) or by adding comments (clarifications).

If the requirement is in a Linear card, edit the linear card. 
If the requirement is from a text file, edit the text file.

## Architecture

Given your understanding of what will be built, you will now proceed to developing the architecture of the feature. The architecture document should map what is being built, the components, the dependencies, the patterns, the technologies, the constraints, the assumptions, the trade-offs, the alternatives, the consequences.

This is where you will put your ultra thinking hat and consider the best path to build the feature, while also considering the patterns and best practices for this project. 

In this section, you are expected to go through the relevant source code, understand its structure and its purpose, and then build an architecture that aligns with the project's patterns and best practices.

Tips:
   - Find specific files based on discovery answers
   - Read relevant code
   - Deep dive into similar features and patterns
   - Analyze specific implementation details
   - Use WebSearch and or context7 for best practices or library documentation (if required)

Your architecture document should include:
    - A high-level overview of the system (before and after the change)
    - Affected components and their relationships, dependencies
    - Patterns and best practices that will be kept or introduced
    - External dependencies that will be used or that need to be added to the project
    - Constraints and assumptions
    - Trade-offs and alternatives
    - Negative consequences (if any) to implementing this design
    - List of the top files to be edited/created

If it helps to build a MERMAID diagram, feel free to do so. 

If, at any point, you have questions or if you find something that contradicts what you previously understood, ask the human for clarification.

Once you have a good understanding of what is being built, save it in the .claude/sessions/<feature_slug>/architecture.md file and ask the human to review it.

If the human agrees with your understanding, you can proceed to the next step. Otherwise, keep iterating together until you get explicit approval to  move forward.

Once the architecture.md is finished, state to the human that you are ready to proceed to the next step.

## Research

If you are not sure how a specific library work, you can use Context7 and Perplexity to search for information about it. So, do not try to guess.

<feature_slug>
#$ARGUMENTS
</feature_slug>
