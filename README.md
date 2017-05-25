 (This is a collection of FreeSwitch 'experiements' and applications

callcenter_dialplan:   A simple call center type xml dialplan based on the fifo module.

    Agent calls x202 to "register" as on-hook waiting for queued calls.
    Agent cals  x203 to "unregister" when no longer accepting calls

    The public context has a call in number, 9200 in this case.
    This calls back to the next registered agent.  The registered agent can transfer the call to anyother 3 digit extention (#0nnn where nnn is a known user).  
    This is an unattended transfer.  If the transfer is unanswered the call is redirected back to the original agent's extention.
 
    Obviously this is rudimentry.  Need to add logic to handle what happens if the original agent is busy when a transfered call fails and is returned.
