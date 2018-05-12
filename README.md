

```python
import pandas as pd
import numpy as np
```


```python
csv_file = "purchase_data.json"
p_data = pd.read_json(csv_file)
p_data
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Gender</th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Price</th>
      <th>SN</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>38</td>
      <td>Male</td>
      <td>165</td>
      <td>Bone Crushing Silver Skewer</td>
      <td>3.37</td>
      <td>Aelalis34</td>
    </tr>
    <tr>
      <th>1</th>
      <td>21</td>
      <td>Male</td>
      <td>119</td>
      <td>Stormbringer, Dark Blade of Ending Misery</td>
      <td>2.32</td>
      <td>Eolo46</td>
    </tr>
    <tr>
      <th>2</th>
      <td>34</td>
      <td>Male</td>
      <td>174</td>
      <td>Primitive Blade</td>
      <td>2.46</td>
      <td>Assastnya25</td>
    </tr>
    <tr>
      <th>3</th>
      <td>21</td>
      <td>Male</td>
      <td>92</td>
      <td>Final Critic</td>
      <td>1.36</td>
      <td>Pheusrical25</td>
    </tr>
    <tr>
      <th>4</th>
      <td>23</td>
      <td>Male</td>
      <td>63</td>
      <td>Stormfury Mace</td>
      <td>1.27</td>
      <td>Aela59</td>
    </tr>
    <tr>
      <th>5</th>
      <td>20</td>
      <td>Male</td>
      <td>10</td>
      <td>Sleepwalker</td>
      <td>1.73</td>
      <td>Tanimnya91</td>
    </tr>
    <tr>
      <th>6</th>
      <td>20</td>
      <td>Male</td>
      <td>153</td>
      <td>Mercenary Sabre</td>
      <td>4.57</td>
      <td>Undjaskla97</td>
    </tr>
    <tr>
      <th>7</th>
      <td>29</td>
      <td>Female</td>
      <td>169</td>
      <td>Interrogator, Blood Blade of the Queen</td>
      <td>3.32</td>
      <td>Iathenudil29</td>
    </tr>
    <tr>
      <th>8</th>
      <td>25</td>
      <td>Male</td>
      <td>118</td>
      <td>Ghost Reaver, Longsword of Magic</td>
      <td>2.77</td>
      <td>Sondenasta63</td>
    </tr>
    <tr>
      <th>9</th>
      <td>31</td>
      <td>Male</td>
      <td>99</td>
      <td>Expiration, Warscythe Of Lost Worlds</td>
      <td>4.53</td>
      <td>Hilaerin92</td>
    </tr>
    <tr>
      <th>10</th>
      <td>24</td>
      <td>Male</td>
      <td>57</td>
      <td>Despair, Favor of Due Diligence</td>
      <td>3.81</td>
      <td>Chamosia29</td>
    </tr>
    <tr>
      <th>11</th>
      <td>20</td>
      <td>Male</td>
      <td>47</td>
      <td>Alpha, Reach of Ending Hope</td>
      <td>1.55</td>
      <td>Sally64</td>
    </tr>
    <tr>
      <th>12</th>
      <td>30</td>
      <td>Male</td>
      <td>81</td>
      <td>Dreamkiss</td>
      <td>4.06</td>
      <td>Iskossa88</td>
    </tr>
    <tr>
      <th>13</th>
      <td>23</td>
      <td>Male</td>
      <td>77</td>
      <td>Piety, Guardian of Riddles</td>
      <td>3.68</td>
      <td>Seorithstilis90</td>
    </tr>
    <tr>
      <th>14</th>
      <td>40</td>
      <td>Male</td>
      <td>44</td>
      <td>Bonecarvin Battle Axe</td>
      <td>2.46</td>
      <td>Sundast29</td>
    </tr>
    <tr>
      <th>15</th>
      <td>21</td>
      <td>Male</td>
      <td>96</td>
      <td>Blood-Forged Skeletal Spine</td>
      <td>4.77</td>
      <td>Haellysu29</td>
    </tr>
    <tr>
      <th>16</th>
      <td>22</td>
      <td>Female</td>
      <td>123</td>
      <td>Twilight's Carver</td>
      <td>1.14</td>
      <td>Sundista85</td>
    </tr>
    <tr>
      <th>17</th>
      <td>22</td>
      <td>Female</td>
      <td>59</td>
      <td>Lightning, Etcher of the King</td>
      <td>1.65</td>
      <td>Aenarap34</td>
    </tr>
    <tr>
      <th>18</th>
      <td>28</td>
      <td>Male</td>
      <td>91</td>
      <td>Celeste</td>
      <td>3.71</td>
      <td>Iskista88</td>
    </tr>
    <tr>
      <th>19</th>
      <td>31</td>
      <td>Male</td>
      <td>177</td>
      <td>Winterthorn, Defender of Shifting Worlds</td>
      <td>4.89</td>
      <td>Assossa43</td>
    </tr>
    <tr>
      <th>20</th>
      <td>24</td>
      <td>Male</td>
      <td>78</td>
      <td>Glimmer, Ender of the Moon</td>
      <td>2.33</td>
      <td>Irith83</td>
    </tr>
    <tr>
      <th>21</th>
      <td>15</td>
      <td>Male</td>
      <td>3</td>
      <td>Phantomlight</td>
      <td>1.79</td>
      <td>Iaralrgue74</td>
    </tr>
    <tr>
      <th>22</th>
      <td>11</td>
      <td>Female</td>
      <td>11</td>
      <td>Brimstone</td>
      <td>2.52</td>
      <td>Deural48</td>
    </tr>
    <tr>
      <th>23</th>
      <td>19</td>
      <td>Male</td>
      <td>183</td>
      <td>Dragon's Greatsword</td>
      <td>2.36</td>
      <td>Chanosia65</td>
    </tr>
    <tr>
      <th>24</th>
      <td>11</td>
      <td>Male</td>
      <td>65</td>
      <td>Conqueror Adamantite Mace</td>
      <td>1.96</td>
      <td>Qarwen67</td>
    </tr>
    <tr>
      <th>25</th>
      <td>21</td>
      <td>Male</td>
      <td>63</td>
      <td>Stormfury Mace</td>
      <td>1.27</td>
      <td>Idai61</td>
    </tr>
    <tr>
      <th>26</th>
      <td>29</td>
      <td>Male</td>
      <td>132</td>
      <td>Persuasion</td>
      <td>3.90</td>
      <td>Aerithllora36</td>
    </tr>
    <tr>
      <th>27</th>
      <td>34</td>
      <td>Male</td>
      <td>106</td>
      <td>Crying Steel Sickle</td>
      <td>2.29</td>
      <td>Assastnya25</td>
    </tr>
    <tr>
      <th>28</th>
      <td>15</td>
      <td>Male</td>
      <td>49</td>
      <td>The Oculus, Token of Lost Worlds</td>
      <td>4.23</td>
      <td>Ilariarin45</td>
    </tr>
    <tr>
      <th>29</th>
      <td>16</td>
      <td>Female</td>
      <td>45</td>
      <td>Glinting Glass Edge</td>
      <td>2.46</td>
      <td>Phaedai25</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>750</th>
      <td>23</td>
      <td>Male</td>
      <td>86</td>
      <td>Stormfury Lantern</td>
      <td>1.28</td>
      <td>Eollym91</td>
    </tr>
    <tr>
      <th>751</th>
      <td>26</td>
      <td>Female</td>
      <td>179</td>
      <td>Wolf, Promise of the Moonwalker</td>
      <td>1.88</td>
      <td>Lisjasksda68</td>
    </tr>
    <tr>
      <th>752</th>
      <td>15</td>
      <td>Female</td>
      <td>116</td>
      <td>Renewed Skeletal Katana</td>
      <td>2.37</td>
      <td>Yalostiphos68</td>
    </tr>
    <tr>
      <th>753</th>
      <td>20</td>
      <td>Male</td>
      <td>4</td>
      <td>Bloodlord's Fetish</td>
      <td>2.28</td>
      <td>Thryallym62</td>
    </tr>
    <tr>
      <th>754</th>
      <td>31</td>
      <td>Male</td>
      <td>104</td>
      <td>Gladiator's Glaive</td>
      <td>1.36</td>
      <td>Sondastan54</td>
    </tr>
    <tr>
      <th>755</th>
      <td>22</td>
      <td>Female</td>
      <td>179</td>
      <td>Wolf, Promise of the Moonwalker</td>
      <td>1.88</td>
      <td>Ailaesuir66</td>
    </tr>
    <tr>
      <th>756</th>
      <td>22</td>
      <td>Male</td>
      <td>6</td>
      <td>Rusty Skull</td>
      <td>1.20</td>
      <td>Siasri67</td>
    </tr>
    <tr>
      <th>757</th>
      <td>35</td>
      <td>Male</td>
      <td>11</td>
      <td>Brimstone</td>
      <td>2.52</td>
      <td>Seosri62</td>
    </tr>
    <tr>
      <th>758</th>
      <td>20</td>
      <td>Male</td>
      <td>122</td>
      <td>Unending Tyranny</td>
      <td>1.21</td>
      <td>Ryastycal90</td>
    </tr>
    <tr>
      <th>759</th>
      <td>19</td>
      <td>Male</td>
      <td>87</td>
      <td>Deluge, Edge of the West</td>
      <td>2.20</td>
      <td>Chanirrasta87</td>
    </tr>
    <tr>
      <th>760</th>
      <td>29</td>
      <td>Male</td>
      <td>81</td>
      <td>Dreamkiss</td>
      <td>4.06</td>
      <td>Aerithllora36</td>
    </tr>
    <tr>
      <th>761</th>
      <td>28</td>
      <td>Male</td>
      <td>175</td>
      <td>Woeful Adamantite Claymore</td>
      <td>1.24</td>
      <td>Raeduerin33</td>
    </tr>
    <tr>
      <th>762</th>
      <td>36</td>
      <td>Male</td>
      <td>52</td>
      <td>Hatred</td>
      <td>4.39</td>
      <td>Lisosiast26</td>
    </tr>
    <tr>
      <th>763</th>
      <td>27</td>
      <td>Other / Non-Disclosed</td>
      <td>48</td>
      <td>Rage, Legacy of the Lone Victor</td>
      <td>4.32</td>
      <td>Eurisuru25</td>
    </tr>
    <tr>
      <th>764</th>
      <td>25</td>
      <td>Male</td>
      <td>70</td>
      <td>Hope's End</td>
      <td>3.89</td>
      <td>Assassasda84</td>
    </tr>
    <tr>
      <th>765</th>
      <td>15</td>
      <td>Male</td>
      <td>13</td>
      <td>Serenity</td>
      <td>1.49</td>
      <td>Aerithnucal56</td>
    </tr>
    <tr>
      <th>766</th>
      <td>22</td>
      <td>Female</td>
      <td>84</td>
      <td>Arcane Gem</td>
      <td>2.23</td>
      <td>Nitherian58</td>
    </tr>
    <tr>
      <th>767</th>
      <td>20</td>
      <td>Male</td>
      <td>122</td>
      <td>Unending Tyranny</td>
      <td>1.21</td>
      <td>Hailaphos89</td>
    </tr>
    <tr>
      <th>768</th>
      <td>21</td>
      <td>Male</td>
      <td>158</td>
      <td>Darkheart, Butcher of the Champion</td>
      <td>3.56</td>
      <td>Chamucosda93</td>
    </tr>
    <tr>
      <th>769</th>
      <td>24</td>
      <td>Male</td>
      <td>73</td>
      <td>Ritual Mace</td>
      <td>3.74</td>
      <td>Frichilsasya78</td>
    </tr>
    <tr>
      <th>770</th>
      <td>22</td>
      <td>Male</td>
      <td>141</td>
      <td>Persuasion</td>
      <td>3.27</td>
      <td>Aenasu69</td>
    </tr>
    <tr>
      <th>771</th>
      <td>24</td>
      <td>Male</td>
      <td>25</td>
      <td>Hero Cane</td>
      <td>1.03</td>
      <td>Lassista97</td>
    </tr>
    <tr>
      <th>772</th>
      <td>15</td>
      <td>Male</td>
      <td>31</td>
      <td>Trickster</td>
      <td>2.07</td>
      <td>Sidap51</td>
    </tr>
    <tr>
      <th>773</th>
      <td>21</td>
      <td>Male</td>
      <td>44</td>
      <td>Bonecarvin Battle Axe</td>
      <td>2.46</td>
      <td>Chamadarsda63</td>
    </tr>
    <tr>
      <th>774</th>
      <td>24</td>
      <td>Male</td>
      <td>123</td>
      <td>Twilight's Carver</td>
      <td>1.14</td>
      <td>Lassassast73</td>
    </tr>
    <tr>
      <th>775</th>
      <td>22</td>
      <td>Male</td>
      <td>98</td>
      <td>Deadline, Voice Of Subtlety</td>
      <td>3.62</td>
      <td>Eural50</td>
    </tr>
    <tr>
      <th>776</th>
      <td>14</td>
      <td>Male</td>
      <td>104</td>
      <td>Gladiator's Glaive</td>
      <td>1.36</td>
      <td>Lirtossa78</td>
    </tr>
    <tr>
      <th>777</th>
      <td>20</td>
      <td>Male</td>
      <td>117</td>
      <td>Heartstriker, Legacy of the Light</td>
      <td>4.15</td>
      <td>Tillyrin30</td>
    </tr>
    <tr>
      <th>778</th>
      <td>20</td>
      <td>Male</td>
      <td>75</td>
      <td>Brutality Ivory Warmace</td>
      <td>1.72</td>
      <td>Quelaton80</td>
    </tr>
    <tr>
      <th>779</th>
      <td>23</td>
      <td>Female</td>
      <td>107</td>
      <td>Splitter, Foe Of Subtlety</td>
      <td>3.61</td>
      <td>Alim85</td>
    </tr>
  </tbody>
</table>
<p>780 rows × 6 columns</p>
</div>




```python
#Player Count
players = len(p_data['SN'].unique())
players_df = pd.DataFrame([{'Total Players': players}])

players_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Players</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>573</td>
    </tr>
  </tbody>
</table>
</div>




```python


```


```python
#Number of Unique Items
remove_duplicates = p_data.drop_duplicates(['Item ID'], keep = 'last')
```


```python
total_items = len(remove_duplicates)
total_items_df = pd.DataFrame([{'Total Items': total_items}])

total_items_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Items</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>183</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Average Purchase Price
average_purchase_price = (p_data['Price'].sum()/p_data['Price'].count()).round(2)
average_purchase_price_df = pd.DataFrame([{'Price': average_purchase_price}])

average_purchase_price_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2.93</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Total Number of Purchases
total_purchases = p_data['Price'].count()
total_purchases_df = pd.DataFrame([{'Total Purchases': total_purchases}])
total_purchases_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Purchases</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>780</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Total Revenue
total_revenue = p_data['Price'].sum()
total_revenue_df = pd.DataFrame([{'Total Revenue': total_revenue}])
total_revenue_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Revenue</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2286.33</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Purchasing Analysis (Total)

p_analysis_df = pd.DataFrame([{
    
    'Number of Unique Items': total_items,
    'Average Purchase Price': average_purchase_price,
    'Total Purchases': total_purchases,
    'Total Revenue': total_revenue
}])
p_analysis_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Average Purchase Price</th>
      <th>Number of Unique Items</th>
      <th>Total Purchases</th>
      <th>Total Revenue</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2.93</td>
      <td>183</td>
      <td>780</td>
      <td>2286.33</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Gender Demographics

#total players = players

# Percentage and Count of Male Players
male_players = p_data[p_data["Gender"] == "Male"]["SN"].nunique()
m_percent = ((male_players/players)*100)
# Percentage and Count of Female Players
female_players = p_data[p_data["Gender"] == "Female"]["SN"].nunique()
f_percent = ((female_players/players)*100)
#Percentage and Count of Other / Non-Disclosed
other_players = p_data[p_data["Gender"] == "Other / Non-Disclosed"]["SN"].nunique()
o_percent = ((other_players/players)*100)
# Gender Demographics
gender_df = pd.DataFrame({"Gender": ["Male", "Female", "Other / Non-Disclosed"], "Percentage of Players": [m_percent, f_percent, o_percent],"Total Count": [male_players, female_players, other_players]})
gender_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender</th>
      <th>Percentage of Players</th>
      <th>Total Count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>81.151832</td>
      <td>465</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Female</td>
      <td>17.452007</td>
      <td>100</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Other / Non-Disclosed</td>
      <td>1.396161</td>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>




```python


```


```python
#Purchasing Analysis (Gender)
#Male purchase count
male_purchases = p_data[p_data["Gender"] == "Male"]["Price"].count()
#Female purchase count
female_purchases = p_data[p_data["Gender"] == "Female"]["Price"].count()
#Other purchase count
other_purchases = p_data[p_data["Gender"] == "Other / Non-Disclosed"]["Price"].count()
#Male Average Purchase Price
ave_male_p = p_data[p_data["Gender"] == "Male"]["Price"].mean()
#Female Average Purchase Price
ave_female_p = p_data[p_data["Gender"] == "Female"]["Price"].mean()
#Other Average Purchase Price
ave_other_p = p_data[p_data["Gender"] == "Other / Non-Disclosed"]["Price"].mean()
#Male Total Purchase Value
total_male_p = p_data[p_data["Gender"] == "Male"]["Price"].sum()
#Female Total Purchase Value
total_female_p = p_data[p_data["Gender"] == "Female"]["Price"].sum()
#Other Total Purchase Value
total_other_p = p_data[p_data["Gender"] == "Other / Non-Disclosed"]["Price"].sum()
#Male Normalized Totals
normal_male_t = total_male_p/male_players
#Female Normalized Totals
normal_female_t = total_female_p/female_players
#Other Normalized Totals
normal_other_t = total_other_p/other_players
gender_analysis_df = pd.DataFrame({"Gender": ["Male", "Female", "Other / Non-Disclosed"], "Purchase Count": [male_purchases, female_purchases, other_purchases],
                                        "Average Purchase Price": [ave_male_p, ave_female_p, ave_other_p], "Total Purchase Value": [total_male_p, total_female_p, total_other_p],
                                "Normalized Totals": [normal_male_t, normal_female_t, normal_other_t]}, columns = 
                                        ["Gender", "Purchase Count", "Average Purchase Price", "Total Purchase Value", "Normalized Totals"])
gender_analysis_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Gender</th>
      <th>Purchase Count</th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
      <th>Normalized Totals</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>633</td>
      <td>2.950521</td>
      <td>1867.68</td>
      <td>4.016516</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Female</td>
      <td>136</td>
      <td>2.815515</td>
      <td>382.91</td>
      <td>3.829100</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Other / Non-Disclosed</td>
      <td>11</td>
      <td>3.249091</td>
      <td>35.74</td>
      <td>4.467500</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Age Demographics

#unique
ten_under = p_data[p_data["Age"] <10]["SN"].nunique()
ten_up = p_data[(p_data["Age"] >=10) & (p_data["Age"] <=14)]["SN"].nunique()
fifteen_up = p_data[(p_data["Age"] >=15) & (p_data["Age"] <=19)]["SN"].nunique()
twenty_up = p_data[(p_data["Age"] >=20) & (p_data["Age"] <=24)]["SN"].nunique()
twentyfive_up = p_data[(p_data["Age"] >=25) & (p_data["Age"] <=29)]["SN"].nunique()
thirty_up = p_data[(p_data["Age"] >=30) & (p_data["Age"] <=34)]["SN"].nunique()
thirty_five_up = p_data[(p_data["Age"] >=35) & (p_data["Age"] <=39)]["SN"].nunique()
forty_up = p_data[(p_data["Age"] >=40) & (p_data["Age"] <=44)]["SN"].nunique()
fortyfive_up = p_data[(p_data["Age"] >=45) & (p_data["Age"] <=49)]["SN"].nunique()

#Purchase Count
c_ten_under = p_data[p_data["Age"] <10]["Price"].count()
c_ten_up = p_data[(p_data["Age"] >=10) & (p_data["Age"] <=14)]["Price"].count()
c_fifteen_up = p_data[(p_data["Age"] >=15) & (p_data["Age"] <=19)]["Price"].count()
c_twenty_up = p_data[(p_data["Age"] >=20) & (p_data["Age"] <=24)]["Price"].count()
c_twentyfive_up = p_data[(p_data["Age"] >=25) & (p_data["Age"] <=29)]["Price"].count()
c_thirty_up = p_data[(p_data["Age"] >=30) & (p_data["Age"] <=34)]["Price"].count()
c_thirty_five_up = p_data[(p_data["Age"] >=35) & (p_data["Age"] <=39)]["Price"].count()
c_forty_up = p_data[(p_data["Age"] >=40) & (p_data["Age"] <=44)]["Price"].count()
c_fortyfive_up = p_data[(p_data["Age"] >=45) & (p_data["Age"] <=49)]["Price"].count()
#Average Purchase Price
a_ten_under = p_data[p_data["Age"] <10]["Price"].mean()
a_ten_up = p_data[(p_data["Age"] >=10) & (p_data["Age"] <=14)]["Price"].mean()
a_fifteen_up = p_data[(p_data["Age"] >=15) & (p_data["Age"] <=19)]["Price"].mean()
a_twenty_up = p_data[(p_data["Age"] >=20) & (p_data["Age"] <=24)]["Price"].mean()
a_twentyfive_up = p_data[(p_data["Age"] >=25) & (p_data["Age"] <=29)]["Price"].mean()
a_thirty_up = p_data[(p_data["Age"] >=30) & (p_data["Age"] <=34)]["Price"].mean()
a_thirty_five_up = p_data[(p_data["Age"] >=35) & (p_data["Age"] <=39)]["Price"].mean()
a_forty_up = p_data[(p_data["Age"] >=40) & (p_data["Age"] <=44)]["Price"].mean()
a_fortyfive_up = p_data[(p_data["Age"] >=45) & (p_data["Age"] <=49)]["Price"].mean()
#Total Purchase Value
t_ten_under = p_data[p_data["Age"] <10]["Price"].sum()
t_ten_up = p_data[(p_data["Age"] >=10) & (p_data["Age"] <=14)]["Price"].sum()
t_fifteen_up = p_data[(p_data["Age"] >=15) & (p_data["Age"] <=19)]["Price"].sum()
t_twenty_up = p_data[(p_data["Age"] >=20) & (p_data["Age"] <=24)]["Price"].sum()
t_twentyfive_up = p_data[(p_data["Age"] >=25) & (p_data["Age"] <=29)]["Price"].sum()
t_thirty_up = p_data[(p_data["Age"] >=30) & (p_data["Age"] <=34)]["Price"].sum()
t_thirty_five_up = p_data[(p_data["Age"] >=35) & (p_data["Age"] <=39)]["Price"].sum()
t_forty_up = p_data[(p_data["Age"] >=40) & (p_data["Age"] <=44)]["Price"].sum()
t_fortyfive_up = p_data[(p_data["Age"] >=45) & (p_data["Age"] <=49)]["Price"].sum()
#Normalized Totals
n_ten_under = t_ten_under/ten_under
n_ten_up = t_ten_up/ten_up
n_fifteen_up = t_fifteen_up/fifteen_up
n_twenty_up = t_twenty_up/twenty_up
n_twentyfive_up = t_twentyfive_up/twentyfive_up
n_thirty_up = t_thirty_up/thirty_up
n_thirty_five_up = t_thirty_five_up/thirty_five_up
n_forty_up = t_forty_up/forty_up
n_fortyfive_up = t_fortyfive_up/fortyfive_up

a_demographic_df = pd.DataFrame({"Age": ["<10", "10-14", "15-19", "20-24", "25-29", "30-34", "35-39", "40-44", "45-49"],
"Percentage of Players": [(ten_under/players)*100, (ten_up/players)*100, (fifteen_up/players)*100, (twenty_up/players)*100, (twentyfive_up/players)*100, (thirty_up/players)*100, (thirty_five_up/players)*100, (forty_up/players)*100, (fortyfive_up/players)*100],
                        "Total Count": [ten_under, ten_up, fifteen_up, twenty_up, twentyfive_up, thirty_up, thirty_five_up, forty_up, fortyfive_up]
                       })
a_demographic_df
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Percentage of Players</th>
      <th>Total Count</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>&lt;10</td>
      <td>3.315881</td>
      <td>19</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10-14</td>
      <td>4.013962</td>
      <td>23</td>
    </tr>
    <tr>
      <th>2</th>
      <td>15-19</td>
      <td>17.452007</td>
      <td>100</td>
    </tr>
    <tr>
      <th>3</th>
      <td>20-24</td>
      <td>45.200698</td>
      <td>259</td>
    </tr>
    <tr>
      <th>4</th>
      <td>25-29</td>
      <td>15.183246</td>
      <td>87</td>
    </tr>
    <tr>
      <th>5</th>
      <td>30-34</td>
      <td>8.202443</td>
      <td>47</td>
    </tr>
    <tr>
      <th>6</th>
      <td>35-39</td>
      <td>4.712042</td>
      <td>27</td>
    </tr>
    <tr>
      <th>7</th>
      <td>40-44</td>
      <td>1.745201</td>
      <td>10</td>
    </tr>
    <tr>
      <th>8</th>
      <td>45-49</td>
      <td>0.174520</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>




```python

demographic_age_df = pd.DataFrame({"Age": ["<10", "10-14", "15-19", "20-24", "25-29", "30-34", "35-39", "40-44", "45-49"],
"Purchase Count": [c_ten_under, c_ten_up, c_fifteen_up, c_twenty_up, c_twentyfive_up, c_thirty_up, c_thirty_five_up, c_forty_up, c_fortyfive_up],
"Average Purchase Price": [a_ten_under, a_ten_up, a_fifteen_up, a_twenty_up, a_twentyfive_up, a_thirty_up, a_thirty_five_up, a_forty_up, a_fortyfive_up],
"Total Purchase Value": [t_ten_under, t_ten_up, t_fifteen_up, t_twenty_up, t_twentyfive_up, t_thirty_up, t_thirty_five_up, t_forty_up, t_fortyfive_up],
"Normalized Totals": [n_ten_under, n_ten_up, n_fifteen_up, n_twenty_up, n_twentyfive_up, n_thirty_up, n_thirty_five_up, n_forty_up, n_fortyfive_up]                                   
                       },columns = 
                            ["Age", "Purchase Count", "Average Purchase Price", "Total Purchase Value", "Normalized Totals"])
demographic_age_df


```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Age</th>
      <th>Purchase Count</th>
      <th>Average Purchase Price</th>
      <th>Total Purchase Value</th>
      <th>Normalized Totals</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>&lt;10</td>
      <td>28</td>
      <td>2.980714</td>
      <td>83.46</td>
      <td>4.392632</td>
    </tr>
    <tr>
      <th>1</th>
      <td>10-14</td>
      <td>35</td>
      <td>2.770000</td>
      <td>96.95</td>
      <td>4.215217</td>
    </tr>
    <tr>
      <th>2</th>
      <td>15-19</td>
      <td>133</td>
      <td>2.905414</td>
      <td>386.42</td>
      <td>3.864200</td>
    </tr>
    <tr>
      <th>3</th>
      <td>20-24</td>
      <td>336</td>
      <td>2.913006</td>
      <td>978.77</td>
      <td>3.779035</td>
    </tr>
    <tr>
      <th>4</th>
      <td>25-29</td>
      <td>125</td>
      <td>2.962640</td>
      <td>370.33</td>
      <td>4.256667</td>
    </tr>
    <tr>
      <th>5</th>
      <td>30-34</td>
      <td>64</td>
      <td>3.082031</td>
      <td>197.25</td>
      <td>4.196809</td>
    </tr>
    <tr>
      <th>6</th>
      <td>35-39</td>
      <td>42</td>
      <td>2.842857</td>
      <td>119.40</td>
      <td>4.422222</td>
    </tr>
    <tr>
      <th>7</th>
      <td>40-44</td>
      <td>16</td>
      <td>3.189375</td>
      <td>51.03</td>
      <td>5.103000</td>
    </tr>
    <tr>
      <th>8</th>
      <td>45-49</td>
      <td>1</td>
      <td>2.720000</td>
      <td>2.72</td>
      <td>2.720000</td>
    </tr>
  </tbody>
</table>
</div>




```python

                                        

```


```python
#Top Spenders
total_Spent = pd.DataFrame(p_data.groupby('SN')['Price'].sum())
purchases_made = pd.DataFrame(p_data.groupby('SN')['Price'].count())
ave_price_spent = pd.DataFrame(p_data.groupby('SN')['Price'].mean())
top = pd.merge(total_Spent, purchases_made, left_index = True, right_index = True).merge(ave_price_spent, left_index=True, right_index=True)
top.rename(columns = {'Price_x': 'Total Purchase Value', 'Price_y':'Purchase Count', 'Price':'Average Purchase Price'}, inplace = True)
top.sort_values('Total Purchase Value', ascending = False, inplace=True)
top.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Total Purchase Value</th>
      <th>Purchase Count</th>
      <th>Average Purchase Price</th>
    </tr>
    <tr>
      <th>SN</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Undirrala66</th>
      <td>17.06</td>
      <td>5</td>
      <td>3.412000</td>
    </tr>
    <tr>
      <th>Saedue76</th>
      <td>13.56</td>
      <td>4</td>
      <td>3.390000</td>
    </tr>
    <tr>
      <th>Mindimnya67</th>
      <td>12.74</td>
      <td>4</td>
      <td>3.185000</td>
    </tr>
    <tr>
      <th>Haellysu29</th>
      <td>12.73</td>
      <td>3</td>
      <td>4.243333</td>
    </tr>
    <tr>
      <th>Eoda93</th>
      <td>11.58</td>
      <td>3</td>
      <td>3.860000</td>
    </tr>
  </tbody>
</table>
</div>




```python


```


```python
#Most Popular Items
popular = pd.DataFrame(p_data.groupby('Item ID')['Item ID'].count())
popular.sort_values('Item ID', ascending = False, inplace = True)
popular_total = pd.DataFrame(p_data.groupby('Item ID')['Price'].sum())
pop_items = pd.merge(popular, popular_total, left_index = True, right_index = True)
drop_items = p_data.drop_duplicates(['Item ID'], keep = 'last')
top_item = pd.merge(pop_items, no_dup_items, left_index = True, right_on = 'Item ID')
top_item = top_item[['Item ID', 'Item Name', 'Item ID_x', 'Price_y', 'Price_x']]
top_item.rename(columns =  {'Item ID_x': 'Purchase Count', 'Price_y': 'Item Price', 'Price_x': 'Total Purchase Value'}, inplace=True)
top_item.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Purchase Count</th>
      <th>Item Price</th>
      <th>Total Purchase Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>721</th>
      <td>39</td>
      <td>Betrayal, Whisper of Grieving Widows</td>
      <td>11</td>
      <td>2.35</td>
      <td>25.85</td>
    </tr>
    <tr>
      <th>766</th>
      <td>84</td>
      <td>Arcane Gem</td>
      <td>11</td>
      <td>2.23</td>
      <td>24.53</td>
    </tr>
    <tr>
      <th>772</th>
      <td>31</td>
      <td>Trickster</td>
      <td>9</td>
      <td>2.07</td>
      <td>18.63</td>
    </tr>
    <tr>
      <th>761</th>
      <td>175</td>
      <td>Woeful Adamantite Claymore</td>
      <td>9</td>
      <td>1.24</td>
      <td>11.16</td>
    </tr>
    <tr>
      <th>765</th>
      <td>13</td>
      <td>Serenity</td>
      <td>9</td>
      <td>1.49</td>
      <td>13.41</td>
    </tr>
  </tbody>
</table>
</div>




```python


```


```python
#Most Profitable
most_profitable = top_item.sort_values('Total Purchase Value', ascending=False)
most_profitable.head(5)
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Item ID</th>
      <th>Item Name</th>
      <th>Purchase Count</th>
      <th>Item Price</th>
      <th>Total Purchase Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>746</th>
      <td>34</td>
      <td>Retribution Axe</td>
      <td>9</td>
      <td>4.14</td>
      <td>37.26</td>
    </tr>
    <tr>
      <th>705</th>
      <td>115</td>
      <td>Spectral Diamond Doomblade</td>
      <td>7</td>
      <td>4.25</td>
      <td>29.75</td>
    </tr>
    <tr>
      <th>657</th>
      <td>32</td>
      <td>Orenmir</td>
      <td>6</td>
      <td>4.95</td>
      <td>29.70</td>
    </tr>
    <tr>
      <th>716</th>
      <td>103</td>
      <td>Singed Scalpel</td>
      <td>6</td>
      <td>4.87</td>
      <td>29.22</td>
    </tr>
    <tr>
      <th>779</th>
      <td>107</td>
      <td>Splitter, Foe Of Subtlety</td>
      <td>8</td>
      <td>3.61</td>
      <td>28.88</td>
    </tr>
  </tbody>
</table>
</div>


