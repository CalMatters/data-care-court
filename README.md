# CARE Court data by county

Last updated: August 28, 2025

This dataset is based on public record requests by reporters [Marisa Kendall](https://calmatters.org/author/marisa-kendall/) and [Jocelyn Wiener](https://calmatters.org/author/jocelyn-wiener/) to California county courts and behavioral health departments about CARE Court usage. The state established the CARE Court program in 2023 to allow judges to order treatment plans for people in severe psychosis who can’t take care of themselves. All counties implemented the program by Dec 2024.

While some [initial](https://www.dhcs.ca.gov/Documents/CARE-Act-Annual-Report-2025.pdf) [statewide](https://www.chhs.ca.gov/wp-content/uploads/2025/06/CARE-Act-Implementation-Update-July-2025.pdf) numbers are available, CalMatters compiled what appears to be the first detailed look at the program by county.

## Methodology

CARE Court petitions are filed to each county court, which may dismiss them or send them to the county's behavioral health department. County behavioral health does the outreach and reports outcomes back to the court. CalMatters requested the following data from every county court, receiving data from 51 of 58, and most county behavioral health departments. If both replied, some numbers for the same county may not match up depending on communication between the agencies and the date of each response. In some cases, only one agency had a responsive record for a certain field. In the story, CalMatters deferred to court numbers if the numbers didn’t match, since behavioral health may not see the full scope of petitions.

## Data Dictionary

If a field is blank, the agency did not specify. If a field is 0, the agency specified 0. Some counties suppressed some or all numbers if they were below 11. Suppressed fields are denoted with *.

### `county-data-from-courts.csv`
Data reported by the Judicial Council of California and individual county superior courts.

<table>
  <thead>
    <tr>
      <th>Field</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>county</td>
      <td>Name of county; except “Judicial Council of California” which receives reports from all county courts
      </td>
    </tr>
    <tr>
      <td>petitions_filed</td>
      <td>Number of CARE Court petitions filed to the county court. Sometimes multiple petitions may be filed for the same person; this dataset includes total petitions filed.
      </td>
    </tr>
    <tr>
      <td>petitions_percapita</td>
      <td>Number of petitions filed per 100k adult county residents, using 2024 population estimates from the CA Dept. of Finance (CARE Court is for 18+). Calculated by CalMatters.</td>
    </tr>
    <tr>
      <td>petitions_dismissed</td>
      <td>Number of CARE Court petitions dismissed by the court. Petitions are generally dismissed before a CARE agreement or plan is developed, but some counties may have included agreements that ended in dismissals.</td>
    </tr>
    <tr>
      <td>care_agreements</td>
      <td>Number of petitions that turned into voluntary CARE treatment agreements</td>
    </tr>
    <tr>
      <td>care_plans</td>
      <td>Number of petitions that turned into court-ordered CARE plans</td>
    </tr>
    <tr>
      <td>graduations</td>
      <td>Number of graduations from CARE agreements or plans. After one year, the client can either complete the program and graduate, or can extend for up to one more year. Most counties have not implemented CARE Court for at least a year (see `date-started-by-county.csv`), so it is too soon for graduations.</td>
    </tr>
    <tr>
      <td>data_as_of</td>
      <td>YYYY-MM-DD date the data is through, usually when the county court replied. The data request was for data since the beginning of the county’s CARE Court implementation.</td>
    </tr>
    <tr>
      <td>notes</td>
      <td>Any clarifications the court sent with the data</td>
    </tr>
  </tbody>
</table>

### `county-data-from-behavioral-health.csv`
Data reported by county behavioral health departments.

<table>
  <thead>
    <tr>
      <th>Field</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>county</td>
      <td>Name of county
      </td>
    </tr>
    <tr>
      <td>petitions</td>
      <td>Number of CARE Court petitions that behavioral health knew about. Since courts can dismiss petitions before they reach behavioral health, this number may be less than total petitions filed. Sometimes multiple petitions may be filed for the same person; this dataset includes total petitions filed.
      </td>
    </tr>
    <tr>
      <td>petitions_dismissed</td>
      <td>Number of CARE Court petitions dismissed that county behavioral health knew about. Since courts can dismiss petitions before they reach behavioral health, this number may be less than total petitions dismissed. Petitions are generally dismissed before a CARE agreement or plan is developed, but some counties may have included agreements that ended in dismissals.</td>
    </tr>
    <tr>
      <td>care_agreements</td>
      <td>Number of petitions that turned into voluntary CARE treatment agreements</td>
    </tr>
    <tr>
      <td>care_plans</td>
      <td>Number of petitions that turned into court-ordered CARE plans</td>
    </tr>
    <tr>
      <td>graduations</td>
      <td>Number of graduations from CARE agreements or plans. After one year, the client can either complete the program and graduate, or can extend for up to one more year. Most counties have not implemented CARE Court for at least a year (see `date-started-by-county.csv`), so it is too soon for graduations.</td>
    </tr>
    <tr>
      <td>data_as_of</td>
      <td>YYYY-MM-DD date the data is through, usually when the county replied. The data request was for data since the beginning of the county’s CARE Court implementation.</td>
    </tr>
    <tr>
      <td>notes</td>
      <td>Any clarifications the court sent with the data</td>
    </tr>
  </tbody>
</table>

### `date-started-by-county.csv`
For each county, the date it launched its CARE Court, according to [the state](https://www.dhcs.ca.gov/Documents/CARE-Act-Annual-Report-2025.pdf#page=20). All counties were required to begin by Dec 2024.

<table>
  <thead>
    <tr>
      <th>Field</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>county</td>
      <td>Name of county
      </td>
    </tr>
    <tr>
      <td>date_started</td>
      <td>YYYY-MM-DD date the county launched its CARE Court</td>
    </tr>
  </tbody>
</table>

### Waiting for responses
Five counties do not appear in the data files because they did not provide data by publication. CalMatters did not request data from behavioral health for some counties with small populations. All dates are 2025.

<table>
  <thead>
    <tr>
      <th>County</th>
      <th>Court</th>
      <th>Behavioral health</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Calaveras</td>
      <td>Requested Jul 29 and Aug 13</td>
      <td>Did not request</td>
    </tr>
    <tr>
      <td>Del Norte</td>
      <td>Requested Jul 29 and Aug 13</td>
      <td>Did not request</td>
    </tr>
    <tr>
      <td>Humboldt</td>
      <td>Requested Jul 29 and Aug 13</td>
      <td>Requested Aug 14</td>
    </tr>
    <tr>
      <td>Inyo</td>
      <td>Requested Jul 29 and Aug 13</td>
      <td>Did not request</td>
    </tr>
    <tr>
      <td>Ventura</td>
      <td>Requested Jul 31</td>
      <td>Requested Aug 1</td>
    </tr>
  </tbody>
</table>

## Plans for further updates
CalMatters also requested data on petitioners and housing status of clients petitioned. This dataset will be updated when the data is ready.

## Examples of Use
This repo contains data for our story "TKTK."

## Data Use

While the contents of this repo are shared under an Apache 2.0 license, CalMatters/The Markup would appreciate any credit or attribution you're willing to give. We're also interested to learn how you used it, so feel free to [send us a message](<mailto:john@calmatters.org>) if you do. If you have any questions, feel free to [contact us](<mailto:john@calmatters.org>) as well.

CalMatters is a nonpartisan, nonprofit journalism venture committed to explaining how California’s state Capitol works and why it matters.

## License

Copyright 2025 CalMatters

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

[http://www.apache.org/licenses/LICENSE-2.0](http://www.apache.org/licenses/LICENSE-2.0)

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
