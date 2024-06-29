# LangChain 
===========

    -> frameword desgined to simplify intergation of LLMS and apps.
    -> via this your application can communicate with vector dbs, llms,external data.
    -> makes it simple to build ai enabled apps.

# LangChain - components:
========================

    Model I/O ->  need to format prompt in a way so that llm can understand(with proper syntax,symantics,grammer of llm), also formatting the response (it's always raw text from LLM. Need to parse and format it.)

    Memory -> LLMs are stateless(like apis).memory module provides short-term(for that session) memory[adds up in each call , can store it in ram(sqlite,redis,files...)] 
            and long-term(previous convo) memory can be pushed and retrived from database

    Retrival -> brings the context(from external datasources)[like attaching file in chatgpt while asking a question] This will be stord in vector db(after transformation). will be retrived and injected into prompt before sending it to LLM.

    Chains -> creation of complex pipeline by linking chains like prompt,models,functions,context, etc..

    Tools -> for additional capabilities. like getting info from wikipedia,YT

    Agents -> advanced components. leverages capabilties of LLMs to perform highly diversified tasks. This is the one which fills the gaps between User,LLM by providing any additional infor/help required.

        e.g user input: book a cab to airport
                llm: doesn't have idea like to which airport,what time.
                Here agent can help in bring these required details by going through apps like Calendar.
                once got the info, LLM guides agent to book the cab.
                So, agents are like assistants which can perform tasks required by LLM.