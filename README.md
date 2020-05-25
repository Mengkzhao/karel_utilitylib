#Utility lib and const def#
****************************************************
ROUTINES LIST: 2020-05-25 10:35:45
****************************************************
----------------------------------------------------
-- TP DISP                             
----------------------------------------------------
ROUTINE ForceMenu(menu_id:INTEGER) FROM utilitylib
----------------------------------------------------
ROUTINE ClearTpDev(dispid:FILE) FROM utilitylib
----------------------------------------------------
ROUTINE ForceUser FROM utilitylib
----------------------------------------------------
ROUTINE ClearUser FROM utilitylib
----------------------------------------------------
ROUTINE ClearErr FROM utilitylib
----------------------------------------------------
-- SYS VARS                             
----------------------------------------------------
-- This routine gets BOOLEAN type system variable and check operation status
ROUTINE GetSysB(varname: STRING): BOOLEAN FROM utilitylib
----------------------------------------------------------
-- This routine gets INTEGER type system variable and check operation status
ROUTINE GetSysI(varname: STRING): INTEGER FROM utilitylib
----------------------------------------------------------
-- This routine sets BOOLEAN type system variable and check operation status
ROUTINE SetSysB(varname: STRING; value: BOOLEAN) FROM utilitylib
----------------------------------------------------------
-- This routine sets INTEGER type system variable and check operation status
ROUTINE SetSysI(varname: STRING; value: INTEGER) FROM utilitylib
----------------------------------------------------
-- ERR Handling                             
----------------------------------------------------
ROUTINE PostErr(message:STRING;prio:INTEGER) FROM utilitylib
----------------------------------------------------
--   File
----------------------------------------------------
ROUTINE OpenFile(in_file:FILE; file_path:STRING; method:INTEGER):BOOLEAN FROM utilitylib
---------------------------------------------------
ROUTINE CloseFile(in_file:FILE):BOOLEAN FROM utilitylib 
----------------------------------------------------
ROUTINE Getline(lFile:FILE;lLine:STRING) : BOOLEAN FROM utilitylib
----------------------------------------------------
-- LOG                            
----------------------------------------------------
ROUTINE LogPip(in_file:FILE;file_name:STRING;in_string:STRING) FROM utilitylib
-----------------------------------------------------
--  Time
-----------------------------------------------------
ROUTINE GetSysTimeStr :STRING FROM utilitylib
----------------------------------------------------
-- Sring Handling                             
----------------------------------------------------
ROUTINE IntToString(num:INTEGER) : STRING FROM utilitylib
----------------------------------------------------
ROUTINE RealToString(num:REAL) : STRING FROM utilitylib
----------------------------------------------------
ROUTINE IntParse(str:STRING,stat:INTEGER):INTEGER  FROM utilitylib 
----------------------------------------------------
ROUTINE SplitStr(separator:STRING;in_string:STRING;out_str_ary:ARRAY OF STRING;cmd_size:INTEGER;l_stat:INTEGER) FROM utilitylib
----------------------------------------------------
--  Dig Ports
----------------------------------------------------
ROUTINE GetMaxIO :INTEGER FROM utilitylib
----------------------------------------------------
ROUTINE GetMaxFLG :INTEGER FROM utilitylib
----------------------------------------------------
--  TPP ARGUMENTS
----------------------------------------------------
ROUTINE GetIntArg(idx:INTEGER):INTEGER FROM utilitylib 
----------------------------------------------------
ROUTINE GetRealArg(idx:INTEGER):REAL FROM utilitylib
----------------------------------------------------
ROUTINE GetStrArg(idx:INTEGER):STRING FROM utilitylib 
----------------------------------------------------
--  Registers
----------------------------------------------------
ROUTINE GetRealReg(regno:INTEGER):REAL FROM utilitylib 
---------------------------------------------------------
ROUTINE GetIntReg(regno:INTEGER):INTEGER FROM utilitylib 
---------------------------------------------------------
ROUTINE GetMaxReg :INTEGER FROM utilitylib
---------------------------------------------------------
ROUTINE GetMaxPReg :INTEGER FROM utilitylib
---------------------------------------------------------
ROUTINE GetPosReg(idx:INTEGER):XYZWPR FROM utilitylib  
---------------------------------------------------------
ROUTINE SetPosReg(idx:INTEGER;in_pos:XYZWPR) FROM utilitylib 
---------------------------------------------------------
ROUTINE GetStrReg(idx:INTEGER):STRING FROM utilitylib  
----------------------------------------------------
--  Math
----------------------------------------------------
ROUTINE POW(base:REAL;exponent:INTEGER):REAL FROM utilitylib 
----------------------------------------------------
ROUTINE Dec2Bin(input:INTEGER;output:ARRAY OF BOOLEAN) FROM utilitylib
----------------------------------------------------
-- This function routine is a random number generator
-- [IN] : seed
--        This integer must be 
--      - a global variable, should be in CMOS,
--      - initialized with any integer value before 
--        first call to this routine,
--      - provided to this routine by reference, 
--        not value.
-- [OUT] : random number
ROUTINE random(seed : INTEGER) : REAL FROM utilitylib
----------------------------------------------------
ROUTINE xor(param1, param2 : INTEGER) : INTEGER FROM utilitylib
----------------------------------------------------
-- UIF
----------------------------------------------------
ROUTINE setuifurl(url: STRING) FROM utilitylib
----------------------------------------------------
ROUTINE gettpuifurl :STRING FROM utilitylib
----------------------------------------------------
ROUTINE TPForceWide :STRING FROM utilitylib
----------------------------------------------------
--  FRAME/TOOL 
----------------------------------------------------
ROUTINE GetUFrame(inUFrame:INTEGER;outPosition:POSITION) FROM utilitylib
----------------------------------------------------------
ROUTINE GetUTool(inUTool:INTEGER;outPosition:POSITION) FROM utilitylib
----------------------------------------------------------
--Position 
----------------------------------------------------------
ROUTINE SetConf(confstr:STRING):CONFIG FROM utilitylib
**********************************************************
**********************************************************