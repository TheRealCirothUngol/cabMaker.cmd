# cabMaker.cmd

    cabMaker [/Cn /Kn /Fn] source\folder[\file] [destination\folder]          v0.3
  
    Generates .CAB or self-extracting batch script from a source file or folder
    using MakeCab + Expand/Extract (compression) + CertUtil (Base64 encoding).
    
    /Cn compression 0=default=make both and keep smallest, 1=MSZIP, 2=LZX
    /Kn keepSrcDir  0=default=ignore folder, 1=retain source folder in archive
    /Fn fileType    0=default=make archive.cab, 1=make self-extracting.cmd
    -------------------------------------------------------------------------------
    
    v0.3
    Corrected extraction to use Extract/Extrac32 if installed version of
    Expand is lower than 6.x, as previous versions ignore paths in CABs.
    Cleaned up 'best compression' code just a bit by removing redundancies.
    
    v0.2
    Added commandline options, auto-choose MSZIP/LZX best compression,
    and improved the MakeCab.ddf settings.
    
    2018/11/07
