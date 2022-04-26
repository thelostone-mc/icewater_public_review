=================
## ErrorTracker
=================

### Global variables
-   `_dLastError`
-   `_dAccmError`
-   `_iLastTime`

### Constructor
`iLastTime` is set to block timestamp on deploy 


### getLastError
- public function that returns `_dLastError` (last stored )


### getAccumulatedError
- public function that returns `_dAccumError` (last stored )


### calculateError
- internal virtual view function (doesn't modify anything)

### applyError
- internal virtual function
- input param is `dError`, `dAccumError`, `iTimeDelta`

### updateError
- checks to ensure `_iLastTime` != `block.timestamp`
- calculates `iTimeDelta` (diff btwn `block.timestamp` and `_iLastTime` )
- updates `_iLastTime`
- updates `_dLastError` by invoking `calculateError` 
- updates `_dAccumError`
- invokes applyError with `_dLastError`, `dAccumError`, `iTimeDelta`
