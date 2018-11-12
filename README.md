# qs-GeoObject-BackgroundImg
Using Qlik Sense's native GeoObject together with any office/shop/plant plan image

Add this code snippet to your load script:

// Define two functions 
SET fX2Long = Round((RangeMax($2,$3)/2 - $2/2 + $1) * 40075014 / RangeMax($2,$3) - 20037507);
SET fY2Lat = Round((RangeMax($2,$3)/2- $3/2 + $1) * -40075014 / RangeMax($2,$3) + 20037507);

// Usage: $(fX2Long(x,width,height)) and $(fY2Lat(y,width,height))

SET fFullArea = '[[' & Round((RangeMax($1,$2)/2 - $1/2) * 40075014 / RangeMax($1,$2) - 20037507) 
    & ',' & Round((RangeMax($1,$2)/2 - $2/2) * -40075014 / RangeMax($1,$2) + 20037507)
    & '],['  & Round((RangeMax($1,$2)/2 + $1/2 ) * 40075014 / RangeMax($1,$2) - 20037507)
    & ',' & Round((RangeMax($1,$2)/2 + $2/2) * -40075014 / RangeMax($1,$2) + 20037507) & ']]';

// Usage: $(fFullArea(width,height)) 
