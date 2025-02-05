<script setup lang="ts">
import DropSpot from "./components/DropSpot.vue";

const placesPerMap = [
  // Erangel
  ["Zharki", "Shooting Range", "Severny", "Stalber", "Kameshki", "Georgopol", "Rozhok", "Yasnaya Polyana", "Boatyard", "School", "Ruins", "Mansion", "Lipovka", "Prison", "Shelter", "Pochinki", "Gatka", "Hospital", "Mylta", "Mylta Power", "Farm", "Quarry", "Primorsk", "Ferry Pier", "Military Base", "Novorepnoye"],
  // Miramar
  ["Oasis", "Campo Militar", "Tierra Bronca", "La Cobreria", "Cruz del Valle", "Water Treatment", "Crater Fields", "Alcantara", "El Pozo", "San Martin", "Hacienda del Patron", "El Alzahar", "Truck Stop", "Minas Generales", "Graveyard", "Power Grid", "Monte Nuevo", "Pecado", "Cantera", "Impala", "Brick Yard", "Chumacera", "Los Leones", "Puerto Paraiso", "Resort", "Valle del Mar", "Prison", "Partona"],
  // Vikendi
  ["Cosmodrome", "Observatory", "Coal Mine", "Laveni", "Neros", "Dinoland", "Villa", "Train Station", "Lumber Yard", "Trika", "Naznova", "Deka Mesto", "Castle", "Pavilka", "Winery", "Kranik"],
  // Sanhok
  ["Khoa", "Mongnai", "Tat Mok", "Ha Tinh", "Camp Alpha", "Paradise Resort", "Camp Bravo", "Bootcamp", "Ruins", "Bhan", "Lakawi", "Kampong", "Quarry", "Pai Nan", "Tambang", "Cave", "Na Kham", "Sahmee", "Camp Charlie", "Ban Tai", "Docks"],
  // Karakin
  ["Bahr Sahir", "Al Habar", "Bashara", "Hadiqa Nemo", "Al Hayik", "Cargo Ship"],
  // Paramo
  ["Lab", "Capaco", "Atahul", "Helipad", "Makalpa"],
  // Haven
  ["Industrial Park", "Rail Yard", "Steel Mill", "Coal Yards", "Docks", "Residential"],
  // Taego
  ["Army Base", "Shipyard", "Wol Song", "Hae Moo Sa", "Go Dok", "Yong Cheon", "Airport", "Palace", "Terminal", "Ha Po", "Fishing Camp", "Kang Neung", "Ho San", "Buk San Sa", "Ho San Prison", "School", "Oh Hyang", "Song Am", "Hospital"],
  // Deston
  ["Ten Forts", "Carpenter's End", "Swamp", "Los Arcos", "Concert", "Assembly", "Buxley", "Construction Site", "Wind Farm", "Barclift", "Turrita", "Arena", "Cavala", "Hydroelectric Dam", "Lodge", "Ripton", "El Koro", "Sancarna", "Holston Meadows"],
  // Rondo
  ["Min Hu", "Nan Chuan", "Rai An", "Kun Xia", "Hernay Town", "Mu Ho Pan", "Bei Li", "Stadium", "Bamboo", "Jao Tin", "Test Track", "Neox Factory", "Lo Hua Xing", "Mey Ran", "Yu Lin", "Yuo Gu", "Fong Tun", "Dan Ching", "Tu Ling", "Jadena City", "Lan Po", "Hung Shan", "Long Ho", "Rin Jiang", "Tin Long Garden"]
]
</script>

<template>
  <div class="container mx-auto">
    <h1 class="text-4xl font-bold tracking-tight sm:text-5xl md:text-6xl p-6">
    <span class="block text-center">
        PUBG Random Drop Spot
    </span>
    </h1>
    <div class="block text-center">
      <Tabs value="0" scrollable lazy>
        <TabList>
          <Tab value="0">Erangel</Tab>
          <Tab value="1">Miramar</Tab>
          <Tab value="2">Vikendi</Tab>
          <Tab value="3">Sanhok</Tab>
          <Tab value="4">Karakin</Tab>
          <Tab value="5">Paramo</Tab>
          <Tab value="6">Haven</Tab>
          <Tab value="7">Taego</Tab>
          <Tab value="8">Deston</Tab>
          <Tab value="9">Rondo</Tab>
        </TabList>
        <TabPanels>
          <TabPanel value="0">
            <DropSpot :places="placesPerMap[0]"/>
          </TabPanel>
          <TabPanel value="1">
            <DropSpot :places="placesPerMap[1]"/>
          </TabPanel>
          <TabPanel value="2">
            <DropSpot :places="placesPerMap[2]"/>
          </TabPanel>
          <TabPanel value="3">
            <DropSpot :places="placesPerMap[3]"/>
          </TabPanel>
          <TabPanel value="4">
            <DropSpot :places="placesPerMap[4]"/>
          </TabPanel>
          <TabPanel value="5">
            <DropSpot :places="placesPerMap[5]"/>
          </TabPanel>
          <TabPanel value="6">
            <DropSpot :places="placesPerMap[6]"/>
          </TabPanel>
          <TabPanel value="7">
            <DropSpot :places="placesPerMap[7]"/>
          </TabPanel>
          <TabPanel value="8">
            <DropSpot :places="placesPerMap[8]"/>
          </TabPanel>
          <TabPanel value="9">
            <DropSpot :places="placesPerMap[9]"/>
          </TabPanel>
        </TabPanels>
      </Tabs>
    </div>
  </div>
</template>
