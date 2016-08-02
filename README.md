# Threat Central ARB Downloader - linux bash script

##Background
This is a solution for those who have the Threat Central Model Import Connector (MIC) for ArcSight ESM installed in the internal network without access to the internet. The MIC though must have access to Arcsight ESM manager.

##Setup
1) Set an API key in the threatcentral.conf file.
2) Specify the location of the threatcentral.conf file in the conf_file field in the arbdownloader file.
3) Add the arbdownloader script to a cron-job to fetch the files every 5 minutes.

##DMZ side
The script should be running from the DMZ with access to threatcentral.io domain on port 443.

##Internal network
Take the arb files from the DMZ and put them in the MIC directory. E.g. C:\Program Files\ArcSightSmartConnectorsTC\current\user\agent\mic\tcmic\tc.
The connector should automatically process the files and update the active-lists in ESM.

##License
(c) Copyright [2016] Hewlett Packard Enterprise Development LP

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License
