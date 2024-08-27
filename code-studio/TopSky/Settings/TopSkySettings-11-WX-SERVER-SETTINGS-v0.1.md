// ##################################################################
//                 #11 WX SERVER SETTINGS v0.1
// ##################################################################

// MET Settings (METAR, TAF & SIGMET)
HTTP_METAR_Server=https://aviationweather.gov/
HTTP_METAR_Page_Prefix=adds/dataserver_current/httpparam?dataSource=metars&requestType=retrieve&format=xml&stationString=
HTTP_METAR_Page_Suffix=&hoursBeforeNow=1&mostRecentForEachStation=true&fields=raw_text
HTTP_METAR_Data_Prefix=<raw_text>
HTTP_METAR_Data_Suffix=</raw_text>

HTTP_TAF_Server=https://aviationweather.gov/
HTTP_TAF_Page_Prefix=adds/dataserver_current/httpparam?dataSource=tafs&requestType=retrieve&format=xml&stationString=
HTTP_TAF_Page_Suffix=&hoursBeforeNow=1&mostRecentForEachStation=true&fields=raw_text
HTTP_TAF_Data_Prefix=<raw_text>
HTTP_TAF_Data_Suffix=</raw_text>

HTTP_SIGMET_Server=https://aviationweather.gov/
HTTP_SIGMET_Page_Prefix=data/iffdp/
HTTP_SIGMET_Pages=6448
HTTP_SIGMET_Page_Suffix=.txt

WXR_Latitude=54.5
WXR_Latitude_Max=61
WXR_Latitude_Min=48
WXR_Longitude=-2.5
WXR_Longitude_Max=5
WXR_Longitude_Min=-10
WXR_Brightness=20
WXR_Gain=85
WXR_Echo_dBZ_Hi=20
WXR_Echo_dBZ_Med=15
WXR_Echo_dBZ_Lo=12 