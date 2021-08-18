# esx_nty_shops

![alt text](https://media.discordapp.net/attachments/553708167595556876/877574701357101066/unknown.png)
![alt text](https://media.discordapp.net/attachments/553708167595556876/877581510180503572/unknown.png)


This resource based on esx_supermarket, I just changed the UI, optimized and added bunch of stuff.



## Installation
### Instal the resource
If you already have esx_shops, just stop esx_shops( and remove it from server.cfg) and start esx_nty_shops( and add it to server.cfg), otherwise:
- Import `esx_shops.sql` to your database
- Add `start esx_nty_shops` in your `server.cfg`:
```
start esx_nty_shops
```

In the Config u can add a lot of blips, but rember to include them later in the list of blips.
If you create a new shop table in the config, remember to call it the same name in shops as in the config.

### How to add your items in the shop
- Add items to the database: (if using weight system)
```mysql
	INSERT INTO `items` (`name`, `label`, `weight`) VALUES ('banana', 'Banana', 10);
```
- Add items to the shop:
```mysql
	INSERT INTO `shops` (store, item, price) VALUES ('TwentyFourSeven','banana',50);
```
- Add an image for your item in `html/img` folder
- U dont have to add path to the image into `fxmanifest.lua` file, just remeber it to be a .png format
- Restart the resource:
```
refresh
restart esx_nty_shops
```

