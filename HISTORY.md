# History

  2.1.0 - June 19 2014
     - Merged #72 - Add optional returnToHead flag, if true, resources are returned to head of queue (stack like 
       behaviour) upon release (contributed by calibr), also see #68 for further discussion.

  2.0.4 - July 27 2013
     - Merged #64 - Fix for not removing idle objects (contributed by PiotrWpl)

  2.0.3 - January 16 2013
     - Merged #56/#57 - Add optional refreshIdle flag. If false, idle resources at the pool minimum will not be
       destroyed/re-created. (contributed by wshaver)
     - Merged #54 - Factory can be asked to validate pooled objects (contributed by tikonen)

  2.0.2 - October 22 2012
     - Fix #51, #48 - createResource() should check for null clientCb in err case (contributed by pooyasencha)
     - Merged #52 - fix bug of infinite wait when create object aync error (contributed by windyrobin)
     - Merged #53 - change the position of dispense and callback to ensure the time order (contributed by windyrobin)
  
  2.0.1 - August 29 2012
     - Fix #44 - leak of 'err' and 'obj' in createResource()
     - Add devDependencies block to package.json
     - Add travis-ci.org integration
     
  2.0.0 - July 31 2012
     - Non-backwards compatible change: remove adjustCallback
        - acquire() callback must accept two params: (err, obj)
     - Add optional 'min' param to factory object that specifies minimum number of
       resources to keep in pool
     - Merged #38 (package.json/Makefile changes - contributed by strk)

  1.0.12 - June 27 2012
     - Merged #37 (Clear remove idle timer after destroyAllNow - contributed by dougwilson)

  1.0.11 - June 17 2012
     - Merged #36 ("pooled" method to perform function decoration for pooled methods - contributed by cosbynator)

  1.0.10 - May 3 2012
     - Merged #35 (Remove client from availbleObjects on destroy(client) - contributed by blax)

  1.0.9 - Dec 18 2011
     - Merged #25 (add getName() - contributed by BryanDonovan)
     - Merged #27 (remove sys import - contributed by botker)
     - Merged #26 (log levels - contributed by JoeZ99)

  1.0.8 - Nov 16 2011
     - Merged #21 (add getter methods to see pool size, etc. - contributed by BryanDonovan)
     
  1.0.7 - Oct 17 2011
     - Merged #19 (prevent release on the same obj twice - contributed by tkrynski)
     - Merged #20 (acquire() returns boolean indicating whether pool is full - contributed by tilgovi)

  1.0.6 - May 23 2011
     - Merged #13 (support error variable in acquire callback - contributed by tmcw) 
        - Note: This change is backwards compatible.  But new code should use the two
                parameter callback format in pool.create() functions from now on.
     - Merged #15 (variable scope issue in dispense() - contributed by eevans)
     
  1.0.5 - Apr 20 2011
     - Merged #12 (ability to drain pool - contributed by gdusbabek)
     
  1.0.4 - Jan 25 2011
     - Fixed #6 (objects reaped with undefined timeouts)
     - Fixed #7 (objectTimeout issue)

  1.0.3 - Dec 9 2010
     - Added priority queueing (thanks to sylvinus)
     - Contributions from Poetro
       - Name changes to match conventions described here: http://en.wikipedia.org/wiki/Object_pool_pattern
          - borrow() renamed to acquire()
          - returnToPool() renamed to release()
       - destroy() removed from public interface
       - added JsDoc comments
       - Priority queueing enhancements
     
  1.0.2 - Nov 9 2010 
     - First NPM release