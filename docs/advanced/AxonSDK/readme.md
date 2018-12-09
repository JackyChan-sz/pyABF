
# Axon SDK Notes

Axon pCLAMP ABF File Support Pack Download Page:
[Download the Support files for Axon pClamp](http://mdc.custhelp.com/app/answers/detail/a_id/18881/~/axon%E2%84%A2-pclamp%C2%AE-abf-file-support-pack-download-page).
_This link is now broken, and the SDK is distributed as a ZIP with pCLAMP 11_.

_This page was generated automatically by [convert.py](convert.py)_

## ABFFILES.H


 * BOOL **ABF_BuildErrorText**(int nErrorNum, const char *szFileName, char *sTxtBuf, UINT uMaxLen)
 * BOOL **ABF_CalculateCRC**(int nFile, int *pnError)
 * BOOL **ABF_Close**(int nFile, int *pnError)
 * BOOL **ABF_EpisodeFromSynchCount**(int nFile, const ABFFileHeader *pFH, DWORD *pdwSynchCount,                                        DWORD *pdwEpisode, int *pnError)
 * BOOL **ABF_FormatDelta**(const ABFFileHeader *pFH, const ABFDelta *pDelta,                              char *pszText, UINT uTextLen, int *pnError)
 * BOOL **ABF_FormatTag**(int nFile, const ABFFileHeader *pFH, long lTagNumber,                            char *pszBuffer, UINT uSize, int *pnError)
 * BOOL **ABF_GetEpisodeDuration**(int nFile, const ABFFileHeader *pFH, DWORD dwEpisode,                                     double *pdDuration, int *pnError)
 * BOOL **ABF_GetEpisodeFileOffset**(int nFile, const ABFFileHeader *pFH, DWORD dwEpisode,                                       DWORD *pdwFileOffset, int *pnError)
 * BOOL **ABF_GetFileHandle**(int nFile, HANDLE *phHandle, int *pnError)
 * BOOL **ABF_GetFileName**( int nFile, LPSTR pszFilename, UINT uTextLen, int *pnError )
 * BOOL **ABF_GetMissingSynchCount**(int nFile, const ABFFileHeader *pFH, DWORD dwEpisode,                                       DWORD *pdwMissingSynchCount, int *pnError)
 * BOOL **ABF_GetNumSamples**(int nFile, const ABFFileHeader *pFH, DWORD dwEpisode,                                UINT *puNumSamples, int *pnError)
 * BOOL **ABF_GetStartTime**(int nFile, const ABFFileHeader *pFH, int nChannel, DWORD dwEpisode,                               double *pdStartTime, int *pnError)
 * BOOL **ABF_GetTrialDuration**(int nFile, const ABFFileHeader *pFH,                                     double *pdDuration, int *pnError)
 * BOOL **ABF_GetVoiceTag**( int nFile, const ABFFileHeader *pFH, UINT uTag, LPCSTR pszFileName,                               long lDataOffset, ABFVoiceTagInfo *pVTI, int *pnError)
 * BOOL **ABF_GetWaveform**(int nFile, const ABFFileHeader *pFH, UINT uDACChannel, DWORD dwEpisode,                                float *pfBuffer, int *pnError)
 * BOOL **ABF_HasData**(int nFile, const ABFFileHeader *pFH)
 * BOOL **ABF_HasOverlappedData**(int nFile, BOOL *pbHasOverlapped, int *pnError)
 * BOOL **ABF_IsABFFile**(const char *szFileName, int *pnDataFormat, int *pnError)
 * BOOL **ABF_MultiplexRead**(int nFile, const ABFFileHeader *pFH, DWORD dwEpisode,                                void *pvBuffer, UINT *puSizeInSamples, int *pnError)
 * BOOL **ABF_MultiplexWrite**(int nFile, const ABFFileHeader *pFH, UINT uFlags, const void *pvBuffer,                                 DWORD dwEpiStart, UINT uSizeInSamples, int *pnError)
 * BOOL **ABF_ParamReader**( int nFile, ABFFileHeader *pFH, int *pnError)
 * BOOL **ABF_ParamWriter**(const char *pszFilename, ABFFileHeader *pFH, int *pnError)
 * BOOL **ABF_ParseStringAnnotation**( LPCSTR pszAnn, LPSTR pszName, UINT uSizeName,                                         LPSTR pszValue, UINT uSizeValue, int *pnError)
 * BOOL **ABF_PlayVoiceTag**( int nFile, const ABFFileHeader *pFH, UINT uTag, int *pnError)
 * BOOL **ABF_ReadAnnotation**( int nFile, const ABFFileHeader *pFH, DWORD dwIndex,                                  LPSTR pszText, DWORD dwBufSize, int *pnError )
 * BOOL **ABF_ReadChannel**(int nFile, const ABFFileHeader *pFH, int nChannel, DWORD dwEpisode,                              float *pfBuffer, UINT *puNumSamples, int *pnError)
 * BOOL **ABF_ReadDACFileEpi**(int nFile, const ABFFileHeader *pFH, short *pnDACArray,                                UINT nChannel, DWORD dwEpisode, int *pnError)
 * BOOL **ABF_ReadDeltas**(int nFile, const ABFFileHeader *pFH, DWORD dwFirstDelta,                             ABFDelta *pDeltaArray, UINT uNumDeltas, int *pnError)
 * BOOL **ABF_ReadIntegerAnnotation**( int nFile, const ABFFileHeader *pFH, DWORD dwIndex,                                         LPSTR pszName, UINT uSizeName, int *pnValue, int *pnError )
 * BOOL **ABF_ReadOpen**( LPCSTR szFileName, int *phFile, UINT fFlags, ABFFileHeader *pFH,                            UINT *puMaxSamples, DWORD *pdwMaxEpi, int *pnError )
 * BOOL **ABF_ReadRawChannel**(int nFile, const ABFFileHeader *pFH, int nChannel, DWORD dwEpisode,                                 void *pvBuffer, UINT *puNumSamples, int *pnError)
 * BOOL **ABF_ReadScopeConfig**( int nFile, ABFFileHeader *pFH, ABFScopeConfig *pCfg,                                   UINT uMaxScopes, int *pnError)
 * BOOL **ABF_ReadStatisticsConfig**( int nFile, const ABFFileHeader *pFH, ABFScopeConfig *pCfg, int *pnError)
 * BOOL **ABF_ReadStringAnnotation**( int nFile, const ABFFileHeader *pFH, DWORD dwIndex,                                       LPSTR pszName, UINT uSizeName, LPSTR pszValue, UINT uSizeValue,                                       int *pnError )
 * BOOL **ABF_ReadTags**(int nFile, const ABFFileHeader *pFH, DWORD dwFirstTag, ABFTag *pTagArray,                           UINT uNumTags, int *pnError)
 * BOOL **ABF_SaveVoiceTag**( int nFile, LPCSTR pszFileName, long lDataOffset,                               ABFVoiceTagInfo *pVTI, int *pnError)
 * BOOL **ABF_SetChunkSize**( int hFile, ABFFileHeader *pFH, UINT *puMaxSamples, DWORD *pdwMaxEpi, int *pnError )
 * BOOL **ABF_SetEpisodeStart**(int nFile, UINT uEpisode, UINT uEpiStart, int *pnError)
 * BOOL **ABF_SetErrorCallback**(int nFile, ABFCallback fnCallback, void *pvThisPointer, int *pnError)
 * BOOL **ABF_SetOverlap**(int nFile, const ABFFileHeader *pFH, BOOL bAllowOverlap, int *pnError)
 * BOOL **ABF_SynchCountFromEpisode**(int nFile, const ABFFileHeader *pFH, DWORD dwEpisode,                                        DWORD *pdwSynchCount, int *pnError)
 * BOOL **ABF_UpdateEpisodeSamples**(int nFile, const ABFFileHeader *pFH, int nChannel, UINT uEpisode,                                       UINT uStartSample, UINT uNumSamples, float *pfBuffer, int *pnError)
 * BOOL **ABF_UpdateHeader**(int nFile, ABFFileHeader *pFH, int *pnError)
 * BOOL **ABF_UpdateTag**(int nFile, UINT uTag, const ABFTag *pTag, int *pnError)
 * BOOL **ABF_WriteAnnotation**( int nFile, ABFFileHeader *pFH, LPCSTR pszText, int *pnError )
 * BOOL **ABF_WriteDACFileEpi**(int nFile, ABFFileHeader *pFH, UINT uDACChannel, const short *pnDACArray, int *pnError)
 * BOOL **ABF_WriteDelta**(int nFile, ABFFileHeader *pFH, const ABFDelta *pDelta, int *pnError)
 * BOOL **ABF_WriteIntegerAnnotation**( int nFile, ABFFileHeader *pFH, LPCSTR pszName, int nData, int *pnError )
 * BOOL **ABF_WriteOpen**( LPCSTR szFileName, int *phFile, UINT fFlags, ABFFileHeader *pFH, int *pnError )
 * BOOL **ABF_WriteRawData**(int nFile, const void *pvBuffer, DWORD dwSizeInBytes, int *pnError)
 * BOOL **ABF_WriteScopeConfig**( int nFile, ABFFileHeader *pFH, int nScopes,                                    /*const*/ ABFScopeConfig *pCfg, int *pnError)
 * BOOL **ABF_WriteStatisticsConfig**( int nFile, ABFFileHeader *pFH,                                         const ABFScopeConfig *pCfg, int *pnError)
 * BOOL **ABF_WriteStringAnnotation**( int nFile, ABFFileHeader *pFH, LPCSTR pszName, LPCSTR pszData, int *pnError )
 * BOOL **ABF_WriteTag**(int nFile, ABFFileHeader *pFH, const ABFTag *pTag, int *pnError)
 * DWORD **ABF_GetMaxAnnotationSize**( int nFile, const ABFFileHeader *pFH )
 * UINT **ABF_GetActualEpisodes**(int nFile)
 * UINT **ABF_GetActualSamples**(int nFile)
 * void **ABF_Cleanup**(void)
## ABFFIO.DLL

Function Name | Relative Address | Ordinal
--------------|------------------|--------
ABF_BuildErrorText|0x00008430|470 (0x1d6)
ABF_CalculateCRC|0x00009220|980 (0x3d4)
ABF_Close|0x00004300|160 (0xa0)
ABF_EpisodeFromSynchCount|0x00007300|290 (0x122)
ABF_FormatDelta|0x00006ff0|460 (0x1cc)
ABF_FormatTag|0x00006bb0|280 (0x118)
ABF_GetActualEpisodes|0x00007860|700 (0x2bc)
ABF_GetActualSamples|0x000078a0|701 (0x2bd)
ABF_GetEpisodeDuration|0x000078e0|360 (0x168)
ABF_GetEpisodeFileOffset|0x00007530|310 (0x136)
ABF_GetFileHandle|0x00008570|910 (0x38e)
ABF_GetFileName|0x000091d0|960 (0x3c0)
ABF_GetMaxAnnotationSize|0x00009140|630 (0x276)
ABF_GetMissingSynchCount|0x00007600|320 (0x140)
ABF_GetNumSamples|0x00007750|340 (0x154)
ABF_GetStartTime|0x00007a10|350 (0x15e)
ABF_GetSynchArray|0x000085b0|900 (0x384)
ABF_GetTrialDuration|0x00007970|530 (0x212)
ABF_GetVoiceTag|0x000083a0|420 (0x1a4)
ABF_GetWaveform|0x000065e0|250 (0xfa)
ABF_HasData|0x00003c50|150 (0x96)
ABF_HasOverlappedData|0x000076f0|330 (0x14a)
ABF_IsABFFile|0x000038b0|140 (0x8c)
ABF_MultiplexRead|0x00005440|170 (0xaa)
ABF_MultiplexWrite|0x00005790|180 (0xb4)
ABF_ParamReader|0x00003630|540 (0x21c)
ABF_ParamWriter|0x00003760|550 (0x226)
ABF_ParseStringAnnotation|0x00008de0|631 (0x277)
ABF_PlayVoiceTag|0x00017d60|430 (0x1ae)
ABF_ReadAnnotation|0x00008d20|620 (0x26c)
ABF_ReadChannel|0x00005be0|210 (0xd2)
ABF_ReadDACFileEpi|0x00006410|230 (0xe6)
ABF_ReadDeltas|0x00006eb0|450 (0x1c2)
ABF_ReadIntegerAnnotation|0x00008f80|622 (0x26e)
ABF_ReadOpen|0x00003090|110 (0x6e)
ABF_ReadRawChannel|0x00006250|220 (0xdc)
ABF_ReadScopeConfig|0x00007e80|380 (0x17c)
ABF_ReadStatisticsConfig|0x00008250|400 (0x190)
ABF_ReadStringAnnotation|0x00008ea0|621 (0x26d)
ABF_ReadTags|0x000068f0|270 (0x10e)
ABF_SaveVoiceTag|0x00008330|410 (0x19a)
ABF_SetChunkSize|0x000089c0|500 (0x1f4)
ABF_SetEpisodeStart|0x00005af0|520 (0x208)
ABF_SetErrorCallback|0x00008530|480 (0x1e0)
ABF_SetOverlap|0x00008a10|510 (0x1fe)
ABF_SynchCountFromEpisode|0x00007440|300 (0x12c)
ABF_UpdateEpisodeSamples|0x000085f0|490 (0x1ea)
ABF_UpdateHeader|0x00003cf0|130 (0x82)
ABF_UpdateTag|0x00006870|262 (0x106)
ABF_WriteAnnotation|0x00008a60|610 (0x262)
ABF_WriteDACFileEpi|0x00006520|240 (0xf0)
ABF_WriteDelta|0x00006e20|440 (0x1b8)
ABF_WriteIntegerAnnotation|0x00008c00|612 (0x264)
ABF_WriteOpen|0x000039c0|120 (0x78)
ABF_WriteRawData|0x00005b80|190 (0xbe)
ABF_WriteScopeConfig|0x00007af0|370 (0x172)
ABF_WriteStatisticsConfig|0x000080c0|390 (0x186)
ABF_WriteStringAnnotation|0x00008af0|611 (0x263)
ABF_WriteTag|0x000067e0|260 (0x104)
ABFH_CheckScopeConfig|0x0000a5a0|1130 (0x46a)
ABFH_CheckUserList|0x0000f820|1500 (0x5dc)
ABFH_ClipADCUUValue|0x0000ad20|1160 (0x488)
ABFH_ClipDACUUValue|0x0000ae50|1180 (0x49c)
ABFH_ConvertABF2ToABF1Header|0x0000b150|1760 (0x6e0)
ABFH_ConvertFromABF1|0x0000c570|1720 (0x6b8)
ABFH_DisplayRangeToGainOffset|0x0000acc0|1410 (0x582)
ABFH_GainOffsetToDisplayRange|0x0000abb0|1400 (0x578)
ABFH_GetAdaptDuration|0x0000d210|3080 (0xc08)
ABFH_GetADCDisplayRange|0x0000ab70|1140 (0x474)
ABFH_GetADCtoUUFactors|0x0000aa80|1150 (0x47e)
ABFH_GetChannelOffset|0x0000c960|1260 (0x4ec)
ABFH_GetCreatorInfo|0x0000c7e0|1740 (0x6cc)
ABFH_GetDACtoUUFactors|0x0000add0|1170 (0x492)
ABFH_GetDigitalWaveform|0x0000e230|1280 (0x500)
ABFH_GetEpisodeDuration|0x0000f000|1450 (0x5aa)
ABFH_GetEpisodeStartToStart|0x0000f330|1490 (0x5d2)
ABFH_GetEpochDuration|0x0000ca60|1660 (0x67c)
ABFH_GetEpochLevel|0x0000cc20|1670 (0x686)
ABFH_GetEpochLevelRange|0x0000cd60|1680 (0x690)
ABFH_GetEpochLimits|0x0000d6d0|1250 (0x4e2)
ABFH_GetErrorText|0x0000c670|1240 (0x4d8)
ABFH_GetHoldingDuration|0x0000d520|1330 (0x532)
ABFH_GetMathChannelName|0x0000b110|1210 (0x4ba)
ABFH_GetMathValue|0x0000af00|1190 (0x4a6)
ABFH_GetMaxPNSubsweeps|0x0000d050|1690 (0x69a)
ABFH_GetMetaEpisodeDuration|0x0000f270|1480 (0x5c8)
ABFH_GetModifierInfo|0x0000c8e0|1750 (0x6d6)
ABFH_GetNumberOfChangingSweeps|0x0000ea70|1630 (0x65e)
ABFH_GetPNDuration|0x0000f120|1460 (0x5b4)
ABFH_GetPostTrainDuration|0x0000d2c0|1700 (0x6a4)
ABFH_GetPostTrainLevel|0x0000d1a0|1710 (0x6ae)
ABFH_GetTimebase|0x0000e9f0|1310 (0x51e)
ABFH_GetTrainDuration|0x0000f1e0|1470 (0x5be)
ABFH_GetWaveform|0x0000d930|1270 (0x4f6)
ABFH_Initialize|0x00009970|1110 (0x456)
ABFH_InitializeScopeConfig|0x0000a140|1120 (0x460)
ABFH_IsADCLeakSubtracted|0x0000f0c0|1440 (0x5a0)
ABFH_IsConstantDigitalOutput|0x0000eee0|1640 (0x668)
ABFH_IsConstantWaveform|0x0000ec00|1340 (0x53c)
ABFH_IsPNEnabled|0x0000f050|1730 (0x6c2)
ABFH_MSToSynchCount|0x0000c7b0|1430 (0x596)
ABFH_ParamReader|0x0000c560|1220 (0x4c4)
ABFH_ParamWriter|0x0000c590|1230 (0x4ce)
ABFH_SweepLenFromUserLen|0x0000d620|1380 (0x564)
ABFH_SynchCountToMS|0x0000c720|1420 (0x58c)
ABFH_UserLenFromSweepLen|0x0000d660|1390 (0x56e)
ABFU_FixSignalName|0x00017cc0|3070 (0xbfe)
ABFU_FormatDouble|0x00017a10|3020 (0xbcc)
ABFU_FormatHMS|0x00017a40|3025 (0xbd1)
ABFU_GetABFString|0x00017b00|3040 (0xbe0)
ABFU_GetValidSignalNameChars|0x00017c30|3060 (0xbf4)
ABFU_IsValidSignalName|0x00017c40|3050 (0xbea)
ABFU_SetABFString|0x00017ab0|3030 (0xbd6)
INFO_FormatDate|0x00010300|2030 (0x7ee)
INFO_FormatTime|0x00010240|2020 (0x7e4)
INFO_GetBufferSize|0x000177d0|2000 (0x7d0)
INFO_GetInfo|0x00010550|2010 (0x7da)