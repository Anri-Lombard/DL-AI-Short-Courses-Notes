# LangChain for LLM Application Development

## Introduction

The creator of LangChain is Harrison Chase, a former Harvard student.

LangChain is:

- an open-source framework for building LLM applications with either Python or Javascript
- focussed on composition and modularity

It makes the process of making modular components for specific use cases easier.

## Models, Prompts, and Parsers

**Models** refer to the LMM models that are used to generate text.

**Prompts** refer to the inputs that are passed into the model.

- Prompt templates allow for the reuse of good prompts to do specific tasks. Langchain has a set of template prompts that can be used.

**Parsers** refer to the output from the model that needs to be parsed into a format that can be used downstream.

- Prompt templates also support output parsing.
- Output is initially given as a long string, but can be parsed into a dictionary with LangChain.

## Memory

Store past conversations in memory so that it has a more conversational flow.

- The way it stores memory is with ConversationBufferMemory.
- The LLM itself is stateless (it does not remember anything from the past). Wrapper code gives the full conversation so far as context to the LLM so it could generate a response. As a conversation gets longer the context gets longer and becomes expensive to provide. LangChain solves this with ConversationBufferMemory.
