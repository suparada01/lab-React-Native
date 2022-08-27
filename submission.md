# 6310110487 ศุภรดา นนทศรี sec 02
=============
ในไฟล์ App.js จะสร้าง Screen หน้า Home และ Weather โดยจะใช้ library ของ react-native โดยจะติดตั้งผ่าน cmd โดยใช้คำสั่ง yarn add @react-navigation/stack @react-navigation/native
ในการสลับหน้าจอไปมา สามารถทำได้ผ่านการใช้Navigation Library ซึ่งไลบรารีที่ถือเป็น Official จาก React คือ react-navigation

เพิ่มคอมโพเนนต์ ZipCodeScreen
=============
จะใช้ FlatList ซึ่งเป็น Component ของ react-native 
<View>
 <FlatList
    data={availableZipItems}
    keyExtractor={_keyExtractor}
    renderItem={({item}) => <ZipItem {...item} navigation={navigation}/>}
 />
 <StatusBar style="auto" />
 </View>

 WeatherScreen สำหรับหน้าจอแสดงคอมโพเนนต์ Weather
 =============
 โดยใช้คำสั่ง
 fetch(`http://api.openweathermap.org/data/2.5/weather?q=${props.zipCode},th&units=metric&APPID=344be349173296a8f911946b02d5c1a8`)
 
 ![](https://imgur.com/8j3z4v4)

 ![](https://imgur.com/8kWOx5q)

 ![](https://imgur.com/jPhOOsk)