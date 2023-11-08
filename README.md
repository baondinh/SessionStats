# SessionStats
Learning more about the Lua programming language and creating a World of Warcraft addon for practical experience
SessionStats is an addon that tracks changes to character during a play session 
- Experience/level gained
- Gold/Silver/Copper change
- Skill ups
- Overall playtime

---------------
Other Lua Notes: 
Lua is a lightweight, multi-paradigm programming language designed for use in within applications
Tables are the main data structuring mechanism for Lua
- Tables are considered objects in Lua (not a value or variable)
- Tables can represent other data structures such as ordinary arrays, symbol tables, sets, queues, etc.

Array = Index and Value Pairs <br />
Hash Table = Key and Value Pairs <br />

Problem: When a function is inside a Lua table, lexical scoping prevents the table being referred to itself as the table has not been initialized yet. How do you handle self-referential tables in Lua?
Need a variable that refers to itself (self-referential variable)

print(table.function_name(table)); <br />
Above statement will not work

Solution: Lua reads from left to right and has a specific way to handle self-referential tables (or tables with a function inside it that needs to reference the table itself)

print(table:function_name()); <br />
Colon only used with function calls and will automatically supply an invisible self-referential variable to be used with function call


