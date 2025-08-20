
# Engineer Reason

This is the command to trigger the start of planning for a feature.

<arguments>
#$ARGUMENTS
</arguments>

## Analysis

Read throught the context.md and architecture.md files in the .claude/sessions/<feature_slug> folder if not done already. 

Your task now is to create a detailed implementation plan (plan.md) for this feature. The goal for this documentation if to create a phased implementation approach that enables us to build the feature incrementally, testing each phase as we go. And it should also make it possible to resume the work in case our session is interrupted.

The plan.md should divide the implementation in phases, each phase with a chunk of the work that could be accomplished by a human in 2 hours.

The template for the plan.md is:

<plan>
# [FEATURE NAME]

If you are working on this feature, make sure to update this plan.md file as you go. 

## PHASE 1 [Completed ✅]

Details of this part of the feature

### A task that was done [Completed ✅]

Details about the task

### A task that was done [Completed ✅]

Details about the task

### Comments:
- Something that happened and forced us to change paths
- Something we learned during development
- Something we discussed and agreed on

## PHASE 2 [In Progress ⏰]

### A task that needs to be done [In Progress ⏰]

Details about the task

### A task that needs to be done [Not Started ⏳]

Details about the task

## PHASE 3 [Not Started ⏳]

### A task that needs to be done [Not Started ⏳]

Details about the task

### A task that needs to be done [Not Started ⏳]

Details about the task

</plan>


Tips:
   - Use repoprompt:search (if available) to find specific files based on discovery answers
   - Use repoprompt:set_selection and repoprompt:read_selected_files (if available) to batch read relevant code
   - Analyze specific implementation details
   - Use WebSearch and or context7 for best practices or library documentation (if required)

In the event that this research raises a new architecture decision or contradiction with the previous decisions, you will start a discussion about it with the human, agree on the changes and update the architecture.md document for that feature is needed. 

This document should also note which tasks need to be done sequentially or in parallel.

Once the plan.md is finished, state to the human that you are ready to proceed to the next step.

