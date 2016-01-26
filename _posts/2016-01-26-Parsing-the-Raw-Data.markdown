---
layout: post
title: Parsing the Raw Data
---

> All of the analysis for this post was created in [``/notebook/Excel_to_CSV.ipynb``](https://github.com/tonyfast/insight/blob/gh-pages/notebook/Excel_to_CSV.ipynb)
The raw Excel dataset contains __492975__ rows.  __173__ were removed
because they do not have a boro identified. Also, restaurants with less 45 samples were removed; this was only done to create
a more managable dataset for the class.  A total of __76897__ restaurants are being consider; this is 
15.59855976469395% of the raw data.
used for the class.

* The dataset has 18 columns.  The fields  are

    * __CAMIS__

    * __DBA__

    * __BORO__

    * __BUILDING__

    * __STREET__

    * __ZIPCODE__

    * __PHONE__

    * __CUISINE DESCRIPTION__

    * __INSPECTION DATE__

    * __ACTION__

    * __VIOLATION CODE__

    * __VIOLATION DESCRIPTION__

    * __CRITICAL FLAG__

    * __SCORE__

    * __GRADE__

    * __GRADE DATE__

    * __RECORD DATE__

    * __INSPECTION TYPE__


A sample of the table is 

<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>index</th>
      <th>CAMIS</th>
      <th>DBA</th>
      <th>BORO</th>
      <th>BUILDING</th>
      <th>STREET</th>
      <th>ZIPCODE</th>
      <th>PHONE</th>
      <th>CUISINE DESCRIPTION</th>
      <th>INSPECTION DATE</th>
      <th>ACTION</th>
      <th>VIOLATION CODE</th>
      <th>VIOLATION DESCRIPTION</th>
      <th>CRITICAL FLAG</th>
      <th>SCORE</th>
      <th>GRADE</th>
      <th>GRADE DATE</th>
      <th>RECORD DATE</th>
      <th>INSPECTION TYPE</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>30075445</td>
      <td>MORRIS PARK BAKE SHOP</td>
      <td>BRONX</td>
      <td>1007</td>
      <td>MORRIS PARK AVE</td>
      <td>10462</td>
      <td>7188924968</td>
      <td>Bakery</td>
      <td>2015-02-09</td>
      <td>Violations were cited in the following area(s).</td>
      <td>06C</td>
      <td>Food not protected from potential source of co...</td>
      <td>Critical</td>
      <td>6</td>
      <td>A</td>
      <td>2015-02-09</td>
      <td>2015-08-14</td>
      <td>Cycle Inspection / Initial Inspection</td>
    </tr>
    <tr>
      <th>15000</th>
      <td>15000</td>
      <td>40386515</td>
      <td>KARAVAS PIZZA N PITA</td>
      <td>MANHATTAN</td>
      <td>108</td>
      <td>7 AVENUE SOUTH                                ...</td>
      <td>10014</td>
      <td>2128076892</td>
      <td>Pizza</td>
      <td>2014-03-04</td>
      <td>Violations were cited in the following area(s).</td>
      <td>06C</td>
      <td>Food not protected from potential source of co...</td>
      <td>Critical</td>
      <td>12</td>
      <td>A</td>
      <td>2014-03-04</td>
      <td>2015-08-14</td>
      <td>Cycle Inspection / Initial Inspection</td>
    </tr>
    <tr>
      <th>30000</th>
      <td>30000</td>
      <td>40401104</td>
      <td>1020 BAR</td>
      <td>MANHATTAN</td>
      <td>1020</td>
      <td>AMSTERDAM AVENUE                              ...</td>
      <td>10025</td>
      <td>2125313468</td>
      <td>American</td>
      <td>2012-12-27</td>
      <td>Violations were cited in the following area(s).</td>
      <td>07A</td>
      <td>Duties of an officer of the Department interfe...</td>
      <td>Critical</td>
      <td>38</td>
      <td>C</td>
      <td>2012-12-27</td>
      <td>2015-08-14</td>
      <td>Cycle Inspection / Re-inspection</td>
    </tr>
    <tr>
      <th>45000</th>
      <td>45000</td>
      <td>40569633</td>
      <td>BOCCA DI BACCO</td>
      <td>MANHATTAN</td>
      <td>635</td>
      <td>NINTH AVENUE                                  ...</td>
      <td>10036</td>
      <td>2122622525</td>
      <td>Italian</td>
      <td>2012-09-19</td>
      <td>Violations were cited in the following area(s).</td>
      <td>06F</td>
      <td>Wiping cloths soiled or not stored in sanitizi...</td>
      <td>Critical</td>
      <td>33</td>
      <td>NaN</td>
      <td>NaT</td>
      <td>2015-08-14</td>
      <td>Cycle Inspection / Initial Inspection</td>
    </tr>
    <tr>
      <th>60000</th>
      <td>60000</td>
      <td>40677610</td>
      <td>EL MARIACHI RESTAURANT</td>
      <td>QUEENS</td>
      <td>6712</td>
      <td>ROOSEVELT AVENUE</td>
      <td>11377</td>
      <td>7183356744</td>
      <td>Mexican</td>
      <td>2012-08-29</td>
      <td>Violations were cited in the following area(s).</td>
      <td>08A</td>
      <td>Facility not vermin proof. Harborage or condit...</td>
      <td>Not Critical</td>
      <td>22</td>
      <td>NaN</td>
      <td>NaT</td>
      <td>2015-08-14</td>
      <td>Cycle Inspection / Initial Inspection</td>
    </tr>
  </tbody>
</table>

# All of the Boros are accounted for.


* [BRONX](../_data/BRONX.csv) - 6089 rows

* [BROOKLYN](../_data/BROOKLYN.csv) - 18191 rows

* [MANHATTAN](../_data/MANHATTAN.csv) - 32618 rows

* [QUEENS](../_data/QUEENS.csv) - 18933 rows

* [STATEN ISLAND](../_data/STATEN ISLAND.csv) - 1066 rows


