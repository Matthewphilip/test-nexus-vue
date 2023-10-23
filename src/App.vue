<template>
  <main id="app">
    <header>
      <nav class="navbar">Navbar</nav>
    </header>
    <section class="body-container">
      <aside>
        <FilterMenu />
      </aside>
      <section class="products-container">
        <FilterTab />
        <div class="product-container">
          <ProductCard
            v-for="(product, index) in products"
            :key="index"
            :product="product"
          />
        </div>
      </section>
    </section>
    <footer class="button-container">
      <button class="filter-button">
        <img src="./assets/listingsfilter.png" alt="Filter Icon" />Filter
      </button>
    </footer>
  </main>
</template>

<script>
import ProductCard from "./components/ProductCard.vue";
import FilterTab from "./components/FilterTab.vue";
import FilterMenu from "./components/FilterMenu.vue";
import "./app.scss";

export default {
  name: "App",
  components: {
    ProductCard,
    FilterTab,
    FilterMenu,
  },

  data() {
    return {
      products: [
        {
          advert_classification: "USED",
          advertisable_id: 54651,
          card_guid: 14425,
          admin_fee: "0.00",
          attention_grabber: null,
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "RED",
          contents: [],
          company: "Fords Cheshire Limited",
          date_first_registered: "2013-09-12",
          date_mot_expires: "2021-09-11",
          derivative: "1.0 MPI GreenTech SE 5dr",
          description: "",
          doors: "5",
          drivetrain: "Front Wheel Drive",
          engine_size: "999",
          extra_description: "",
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "1E",
          location: "WSLINE",
          location_slug: "wsline",
          make: "Skoda",
          make_slug: "skoda",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "Citigo",
          model_year: null,
          name: "SKODA CITIGO HATCHBACK 1.0 MPI GreenTech SE 5dr",
          odometer_units: "Miles",
          odometer_value: 22425,
          original_price: "4899.00",
          plate: "2013 (63)",
          previous_keepers: 1,
          price: "4799.00",
          price_ex_vat: "4899.00",
          price_when_new: "7437.50",
          range: "Citigo",
          range_slug: "citigo",
          reserved: "Available",
          seats: "4",
          site: "Winsford",
          site_slug: "winsford",
          slug: "skoda-citigo-se-greentech-10-mpi-greentech-se-5dr-00317823",
          standard_equipment: {
            Security: [
              "Electronic engine immobiliser",
              "Locking fuel filler cap",
            ],
            Entertainment: [
              "6 speakers",
              "Aux-in socket",
              "Radio\\/MP3 player",
              "SD card slot",
              "USB socket",
            ],
            "Passive Safety": [
              "3 point height adj front seatbelts + pretensioners",
              "ABS",
              "Driver and passenger airbags",
              "Driver\\/front passenger head+thorax airbag",
              "Driver\\/front passenger side airbags",
              "ESP",
              "Seatbelt warning lamp and buzzer",
              "Two 3 point rear seatbelts",
              "Two tone horn",
              "Tyre pressure monitor",
            ],
            "Exterior Features": [
              "Body colour bumpers",
              "Body colour door mirrors and handles",
              "Chrome grille surround",
              "Daytime running lights",
              "Electric front windows",
              "Heated rear window",
              "Rear wiper",
            ],
            "Interior Features": [
              "12V accessory power point in centre console",
              "60\\/40 split folding rear seat",
              "Boot light",
              "Delay courtesy light function",
              "Directional air vents for side windows",
              "Driver and passenger front seat pockets",
              "Driver seat height adjust",
              "Driver's sunvisor with ticket holder",
              "Front head restraints",
              "Glovebox",
              "Height adjustable rear head restraints",
              "Height adjustable steering wheel",
              "Isofix Preparation 2 Rear child seats",
              "Passenger sunvisor with vanity mirror",
            ],
            "Driver Convenience": [
              "Bluetooth system",
              "Fuel gauge",
              "Rev counter",
              "Service interval indicator",
              "Smart phone holder",
              "Speed sensitive power steering",
            ],
            "Engine\\/Drivetrain\\/Suspension": ["Lowered suspension"],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00317823",
          tags: [],
          tax_rate_value: "0.00",
          technical_data: {
            cc: {
              name: "CC",
              value: "999",
              category: "Engine and Drive Train",
            },
            nox: {
              name: "NOx",
              value: "0.008",
              category: "Emissions - ICE",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            width: {
              name: "Width",
              value: "1645",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "Yes",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "95",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1463",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "3563",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "DOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "100",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "3",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "4",
              category: "Weight and Capacities",
            },
            wheelType: {
              name: "Wheel Type",
              value: '14" ALLOY',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2420",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "60",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "SE",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "57.7",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "No",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "APUS",
              category: "Tyres",
            },
            maxRoofLoad: {
              name: "Max. Roof Load",
              value: "50",
              category: "Weight and Capacities",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "14.4",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            tyreSizeRear: {
              name: "Tyre Size Rear",
              value: "175\\/65 R14",
              category: "Tyres",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.0",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "68.9",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "44",
              category: "Performance",
            },
            noiseLevelDba: {
              name: "Noise Level dB(A)",
              value: "71",
              category: "Emissions - ICE",
            },
            tyreSizeFront: {
              name: "Tyre Size Front",
              value: "175\\/65 R14",
              category: "Tyres",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "TYRE REPAIR KIT",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "60",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "5000",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "95",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "1",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "12",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "MPI GREENTECH",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "74.5",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "76.4",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "10",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "3000",
              category: "Performance",
            },
            compressionRatio: {
              name: "Compression Ratio",
              value: "10:5:1",
              category: "Engine and Drive Train",
            },
            maxLoadingWeight: {
              name: "Max. Loading Weight",
              value: "425",
              category: "Weight and Capacities",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "86",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "76.4",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "70",
              category: "Performance",
            },
            minimumKerbweight: {
              name: "Minimum Kerbweight",
              value: "865",
              category: "Weight and Capacities",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            grossVehicleWeight: {
              name: "Gross Vehicle Weight",
              value: "1290",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 6",
              category: "Emissions - ICE",
            },
            widthIncludingMirrors: {
              name: "Width (including mirrors)",
              value: "1910",
              category: "Vehicle Dimensions",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "35",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "251",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "10000",
              category: "General",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "9.8",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "959",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "46",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "89",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "80",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "1E",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "3",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "5",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "10",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "249.83",
          vat_scheme: "Margin",
          vat_when_new: "1487.50",
          videos: "[]",
          vin: "TMBZZZAAZED609853",
          vrm: "BX63NSJ",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/skoda-citigo-se-greentech-10-mpi-greentech-se-5dr-00317823",
          year: "2013",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082853\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082853\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082853\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082854\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082854\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082854\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082852\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082852\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082852\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082853\\/skoda-citigo-se-greentech-10-mpi-greentech-se-5dr-00317823-wA2yCREz.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082854\\/skoda-citigo-se-greentech-10-mpi-greentech-se-5dr-00317823-O6JUmEos.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1082852\\/skoda-citigo-se-greentech-10-mpi-greentech-se-5dr-00317823-nCI9Ne4X.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [["Bluetooth", "Aux In", "MP3", "Isofix"]],
          wheelchair_access: 0,
        },
        {
          advert_classification: "USED",
          advertisable_id: 54543,
          card_guid: 14344,
          admin_fee: "0.00",
          attention_grabber: 'Sports Seats | 16" Alloys',
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "WHITE",
          contents: [],
          company: "Graham Bell Limited",
          date_first_registered: "2013-05-17",
          date_mot_expires: "2022-06-09",
          derivative: "1.2 SXi 3dr",
          description:
            "*Low mileage Corsa with an eye catching design and beautiful specification* This model is finished in signature Casablanca White with Vauxhall\\u2019s insurance friendly 1.2 petrol engine developing 85 bhp and 115Nm of torque, 5 speed manual transmission, SXI b",
          doors: "3",
          drivetrain: "Front Wheel Drive",
          engine_size: "1229",
          extra_description:
            '[Cruise Control, 16" Alloys, Sports Seats, CD Player]',
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "6E",
          location: "TRAFFORD ROW E",
          location_slug: "trafford-row-e",
          make: "Vauxhall",
          make_slug: "vauxhall",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "Corsa",
          model_year: null,
          name: 'VAUXHALL CORSA HATCHBACK 1.2 SXi 3dr [Cruise Control, 16" Alloys, Sports Seats, CD Player]',
          odometer_units: "Miles",
          odometer_value: 31160,
          original_price: "4999.00",
          plate: "2013 (13)",
          previous_keepers: 1,
          price: "4999.00",
          price_ex_vat: "4999.00",
          price_when_new: "11283.33",
          range: "Corsa",
          range_slug: "corsa",
          reserved: "Available",
          seats: "5",
          site: "Manchester",
          site_slug: "trafford",
          slug: "vauxhall-corsa-sxi-12-sxi-3dr-00317716",
          standard_equipment: {
            Trim: ["Piano black centre console"],
            Packs: ["Technical pack - Corsa"],
            Security: ["Immobiliser", "Remote central deadlocking"],
            Entertainment: ["Steering wheel mounted audio controls"],
            "Passive Safety": [
              "ABS+EBA",
              "Dual stage Driver\\/Passenger Airbags",
              "Electronic stability control",
              "Front passenger airbag deactivation",
              "Hill start assist",
              "Three rear inertia reel lap\\/diagonal seatbelts",
              "Tyre pressure monitoring system",
            ],
            "Exterior Features": [
              "Body colour bumpers",
              "Body colour door handles",
              "Chrome detailing",
              "Dark style headlights",
              "Dark tinted rear glass",
              "Daytime running lights",
              "Door to door illumination",
              "Electric front windows\\/one touch\\/auto reverse",
              "Electrically adjustable door mirrors",
              "Follow me home headlights",
              "Front fog lights",
              "Heated door mirrors",
              "Rear wiper",
              "Tinted glass",
            ],
            "Interior Features": [
              "60\\/40 split folding rear seat",
              "Chrome gear knob",
              "Front reading lights",
              "Front seat back map pockets",
              "Front sports seats",
              "Height adjustable driver's seat",
              "Reach + rake adjustable steering column",
              "Twist cloth upholstery",
            ],
            "Driver Convenience": ["Service interval indicator"],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00317716",
          tags: [],
          tax_rate_value: "130.00",
          technical_data: {
            cc: {
              name: "CC",
              value: "1229",
              category: "Engine and Drive Train",
            },
            co: {
              name: "CO",
              value: "0.301",
              category: "Emissions - ICE",
            },
            hc: {
              name: "HC",
              value: "0.032",
              category: "Emissions - ICE",
            },
            nox: {
              name: "NOx",
              value: "0.025",
              category: "Emissions - ICE",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            hcnox: {
              name: "HC+NOx",
              value: "0.057",
              category: "Emissions - ICE",
            },
            width: {
              name: "Width",
              value: "1713",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "Yes",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "129",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1488",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "3999",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "DOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "107",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "4",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "5",
              category: "Weight and Capacities",
            },
            particles: {
              name: "Particles",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            wheelType: {
              name: "Wheel Type",
              value: '16" ALLOY',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2511",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "85",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "SXi",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "39.2",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "No",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "5 SPOKE SPORTS",
              category: "Tyres",
            },
            maxRoofLoad: {
              name: "Max. Roof Load",
              value: "75",
              category: "Weight and Capacities",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "13.6",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            tyreSizeRear: {
              name: "Tyre Size Rear",
              value: "195\\/55 R16",
              category: "Tyres",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.2",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "51.4",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "63",
              category: "Performance",
            },
            noiseLevelDba: {
              name: "Noise Level dB(A)",
              value: "71",
              category: "Emissions - ICE",
            },
            tyreSizeFront: {
              name: "Tyre Size Front",
              value: "195\\/55 R16",
              category: "Tyres",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "TYRE REPAIR KIT",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "85",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "5600",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "115",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "4",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "16",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "Not Available",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "73.4",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "62.8",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "11.8",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "4000",
              category: "Performance",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "Not Available",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "72.6",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "85",
              category: "Performance",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            grossVehicleWeight: {
              name: "Gross Vehicle Weight",
              value: "1555",
              category: "Weight and Capacities",
            },
            maxTowingWeightBraked: {
              name: "Max. Towing Weight - Braked",
              value: "850",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 5",
              category: "Emissions - ICE",
            },
            widthIncludingMirrors: {
              name: "Width (including mirrors)",
              value: "1944",
              category: "Vehicle Dimensions",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "45",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "285",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "20000",
              category: "General",
            },
            maxTowingWeightUnbraked: {
              name: "Max. Towing Weight - Unbraked",
              value: "450",
              category: "Weight and Capacities",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "10.1",
              category: "Weight and Capacities",
            },
            heightIncludingRoofRails: {
              name: "Height (including roof rails)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "1050",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "Not Available",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            timingBeltIntervalMileage: {
              name: "Timing Belt Interval Mileage",
              value: "100000",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            serviceIntervalFrequencyMonths: {
              name: "Service Interval Frequency - Months",
              value: "12",
              category: "General",
            },
            euroNcapPedestrianTestStarRating: {
              name: "EURO NCAP Pedestrian test - Star Rating.",
              value: "Not Available",
              category: "General",
            },
            timingBeltIntervalFrequencyMonths: {
              name: "Timing Belt Interval Frequency - Months",
              value: "60",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "6E",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "1",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            euroNcapFrontAndSideImpactTestStarRating: {
              name: "EURO NCAP Front and Side Impact test - Star Rating.",
              value: "Not Available",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "6",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "416.50",
          vat_scheme: "Margin",
          vat_when_new: "2256.67",
          videos: "[]",
          vin: "W0L0SDL08D4195278",
          vrm: "MJ13MVG",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716",
          year: "2013",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089364\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089364\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089364\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089365\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089365\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089365\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089372\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089372\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089372\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089355\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089355\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089355\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089358\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089358\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089358\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089359\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089359\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089359\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089362\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089362\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089362\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089373\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089373\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089373\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089375\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089375\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089375\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089377\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089377\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089377\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089379\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089379\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089379\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089368\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089368\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089368\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089370\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089370\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089370\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089366\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089366\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089366\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089364\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-IcQM2jpO.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089365\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-RXWg9qYb.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089372\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-V31ZxOp6.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089355\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-qEdX8PAp.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089358\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-W5N8ewsk.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089359\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-qIdzWZJv.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089362\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-YHs9c7In.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089373\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-26ppC6kk.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089375\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-GUUGKztL.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089377\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-D0uhLQZn.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089379\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-ad6ZrSh0.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089368\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-DMujxM9g.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089370\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-64PPPWWK.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1089366\\/vauxhall-corsa-sxi-12-sxi-3dr-00317716-YVIJWh75.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [[]],
          wheelchair_access: 0,
        },
        {
          advert_classification: "USED",
          advertisable_id: 56394,
          card_guid: 15917,
          admin_fee: "0.00",
          attention_grabber: '8 Speaker Hi-Fi | 15" Alloys',
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "SILVER",
          contents: [],
          company: "Fords Cheshire Limited",
          date_first_registered: "2014-08-20",
          date_mot_expires: "2021-09-14",
          derivative: "1.2 12V SE 5dr",
          description:
            "*Low mileage Fabia with an eye catching design and beautiful specification* This model is finished in premium Brilliant Silver metallic with Skoda\\u2019s insurance friendly 1.2 petrol engine developing 69 bhp and 112Nm of torque (this model benefits from a low",
          doors: "5",
          drivetrain: "Front Wheel Drive",
          engine_size: "1198",
          extra_description:
            '[CD Player, Air Conditioning, 8 Speaker Hi-Fi, 15" Alloys]',
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "5E",
          location: "TRAFFORD ROW D",
          location_slug: "trafford-row-d",
          make: "Skoda",
          make_slug: "skoda",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "Fabia",
          model_year: null,
          name: 'SKODA FABIA HATCHBACK 1.2 12V SE 5dr [CD Player, Air Conditioning, 8 Speaker Hi-Fi, 15" Alloys]',
          odometer_units: "Miles",
          odometer_value: 37600,
          original_price: "4999.00",
          plate: "2014 (14)",
          previous_keepers: 1,
          price: "4999.00",
          price_ex_vat: "4999.00",
          price_when_new: "9512.50",
          range: "Fabia",
          range_slug: "fabia",
          reserved: "Available",
          seats: "5",
          site: "Manchester",
          site_slug: "trafford",
          slug: "skoda-fabia-se-12v-12-12v-se-5dr-00319540",
          standard_equipment: {
            Trim: ["Chrome air vent surrounds"],
            Security: [
              "Alarm with tilt sensor",
              "Immobiliser",
              "Remote central locking",
            ],
            Entertainment: [
              "8 speakers",
              "Auxiliary socket for external MP3 player",
              "Dance 2 DIN radio with CD + MP3",
            ],
            "Passive Safety": [
              "3x3 point rear seatbelts",
              "ABS",
              "Driver and passenger airbags",
              "Driver and passenger side airbags",
              "Driver's seatbelt undone warning light",
              "ESC with ASR",
              "Front seatbelt pretensioners",
              "Passenger airbag deactivate switch",
              "Tyre pressure monitor",
            ],
            "Exterior Features": [
              "Aspherical driver's exterior mirror",
              "Auto dimming interior mirror",
              "Body colour bumpers",
              "Body colour door handles",
              "Body colour door mirrors",
              "Chrome grille surround",
              "Electric front windows",
              "Electrically adjustable and heated door mirrors",
              "Heated rear window",
              "Height adjustable headlamps",
              "Intermittent rear wash\\/wipe",
              "Tinted rear windows",
              "Tinted windscreen",
            ],
            "Interior Features": [
              "1.5L bottle holder in front door panels",
              "2 height adjustable rear headrests",
              "60\\/40 split folding rear seat",
              "Boot stowage box",
              "Cargo area storage tray",
              "Driver + passenger vanity mirrors",
              "Folding grab handles",
              "Height adjustable front headrests",
              "Height adjustable front seats",
              "Height\\/reach adjust steering wheel",
              "Interior light with delay",
              "Internal chrome door handles",
              "Lower glovebox cover",
              "Luggage load hooks",
              "Pollen filter",
              "Rear storage trays",
              "Rear top tether child seat ISOFIX attachment",
              "Ticket holder",
            ],
            "Driver Convenience": [
              "Exterior temperature gauge",
              "PAS",
              "Service interval indicator",
            ],
            "Engine\\/Drivetrain\\/Suspension": ["Sports suspension"],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00319540",
          tags: [],
          tax_rate_value: "130.00",
          technical_data: {
            cc: {
              name: "CC",
              value: "1198",
              category: "Engine and Drive Train",
            },
            co: {
              name: "CO",
              value: "0.696",
              category: "Emissions - ICE",
            },
            hc: {
              name: "HC",
              value: "0.045",
              category: "Emissions - ICE",
            },
            nox: {
              name: "NOx",
              value: "0.016",
              category: "Emissions - ICE",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            hcnox: {
              name: "HC+NOx",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            width: {
              name: "Width",
              value: "1642",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "Yes",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "128",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1498",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "4000",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "DOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "101",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "3",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "5",
              category: "Weight and Capacities",
            },
            particles: {
              name: "Particles",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            wheelType: {
              name: "Wheel Type",
              value: '15" ALLOY',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2465",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "70",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "SE",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "38.7",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "No",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "ANTARES",
              category: "Tyres",
            },
            maxRoofLoad: {
              name: "Max. Roof Load",
              value: "75",
              category: "Weight and Capacities",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "14.9",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            tyreSizeRear: {
              name: "Tyre Size Rear",
              value: "195\\/55 R15",
              category: "Tyres",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.2",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "51.4",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "51",
              category: "Performance",
            },
            noiseLevelDba: {
              name: "Noise Level dB(A)",
              value: "73",
              category: "Emissions - ICE",
            },
            tyreSizeFront: {
              name: "Tyre Size Front",
              value: "195\\/55 R15",
              category: "Tyres",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "TYRE REPAIR KIT",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "69",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "5400",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "112",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "2",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "12",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "12V",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "76.5",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "62.8",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "11",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "3000",
              category: "Performance",
            },
            compressionRatio: {
              name: "Compression Ratio",
              value: "10.5:1",
              category: "Engine and Drive Train",
            },
            maxLoadingWeight: {
              name: "Max. Loading Weight",
              value: "455",
              category: "Weight and Capacities",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "Not Available",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "86.9",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "83",
              category: "Performance",
            },
            minimumKerbweight: {
              name: "Minimum Kerbweight",
              value: "1095",
              category: "Weight and Capacities",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            grossVehicleWeight: {
              name: "Gross Vehicle Weight",
              value: "1550",
              category: "Weight and Capacities",
            },
            maxTowingWeightBraked: {
              name: "Max. Towing Weight - Braked",
              value: "800",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 5",
              category: "Emissions - ICE",
            },
            widthIncludingMirrors: {
              name: "Width (including mirrors)",
              value: "1886",
              category: "Vehicle Dimensions",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "45",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "315",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "10000",
              category: "General",
            },
            maxTowingWeightUnbraked: {
              name: "Max. Towing Weight - Unbraked",
              value: "500",
              category: "Weight and Capacities",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "10",
              category: "Weight and Capacities",
            },
            heightIncludingRoofRails: {
              name: "Height (including roof rails)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "1180",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "Not Available",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "5E",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "3",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "10",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "299.83",
          vat_scheme: "Margin",
          vat_when_new: "1902.50",
          videos: "[]",
          vin: "TMBFH25JXE3112357",
          vrm: "MC14GWY",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540",
          year: "2014",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109153\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109153\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109153\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109155\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109155\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109155\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109161\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109161\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109161\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109162\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109162\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109162\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109164\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109164\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109164\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109167\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109167\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109167\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109169\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109169\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109169\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109172\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109172\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109172\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109174\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109174\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109174\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109175\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109175\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109175\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109176\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109176\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109176\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109150\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109150\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109150\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109159\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109159\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109159\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109157\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109157\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109157\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109153\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-PMMVpIUH.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109155\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-bSrgkWyc.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109161\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-R1QKfl71.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109162\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-UYHjzavT.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109164\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-PNe9rSa8.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109167\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-P7AgJRXq.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109169\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-da95O8Tb.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109172\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-FNLCB2Md.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109174\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-4Q7P2sfv.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109175\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-Fvh8wwjm.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109176\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-nmQMPT6V.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109150\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-lCDWyF4U.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109159\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-HEru8b7R.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1109157\\/skoda-fabia-se-12v-12-12v-se-5dr-00319540-Sed80Eb6.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [["MP3", "Aux In", "Isofix"]],
          wheelchair_access: 0,
        },
        {
          advert_classification: "USED",
          advertisable_id: 55823,
          card_guid: 15458,
          admin_fee: "0.00",
          attention_grabber: null,
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "SILVER",
          contents: [],
          company: "Graham Bell Limited",
          date_first_registered: "2013-03-30",
          date_mot_expires: "2021-10-26",
          derivative: "1.2 12V SE 5dr",
          description: "",
          doors: "5",
          drivetrain: "Front Wheel Drive",
          engine_size: "1198",
          extra_description: "",
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "5E",
          location: "REC F71",
          location_slug: "rec-f71",
          make: "Skoda",
          make_slug: "skoda",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "Fabia",
          model_year: null,
          name: "SKODA FABIA HATCHBACK 1.2 12V SE 5dr",
          odometer_units: "Miles",
          odometer_value: 33820,
          original_price: "4999.00",
          plate: "2013 (13)",
          previous_keepers: 1,
          price: "4999.00",
          price_ex_vat: "4999.00",
          price_when_new: "9087.50",
          range: "Fabia",
          range_slug: "fabia",
          reserved: "Available",
          seats: "5",
          site: "Winsford",
          site_slug: "winsford",
          slug: "skoda-fabia-se-12v-12-12v-se-5dr-00318971",
          standard_equipment: {
            Trim: ["Chrome air vent surrounds"],
            Security: [
              "Alarm with tilt sensor",
              "Immobiliser",
              "Remote central locking",
            ],
            Entertainment: [
              "8 speakers",
              "Auxiliary socket for external MP3 player",
              "Dance 2 DIN radio with CD + MP3",
            ],
            "Passive Safety": [
              "3x3 point rear seatbelts",
              "ABS",
              "Driver and passenger airbags",
              "Driver and passenger side airbags",
              "Driver's seatbelt undone warning light",
              "ESC with ASR",
              "Front seatbelt pretensioners",
              "Passenger airbag deactivate switch",
              "Tyre pressure monitor",
            ],
            "Exterior Features": [
              "Aspherical driver's exterior mirror",
              "Auto dimming interior mirror",
              "Body colour bumpers",
              "Body colour door handles",
              "Body colour door mirrors",
              "Chrome grille surround",
              "Electric front windows",
              "Electrically adjustable and heated door mirrors",
              "Heated rear window",
              "Height adjustable headlamps",
              "Intermittent rear wash\\/wipe",
              "Tinted rear windows",
              "Tinted windscreen",
            ],
            "Interior Features": [
              "1.5L bottle holder in front door panels",
              "2 height adjustable rear headrests",
              "60\\/40 split folding rear seat",
              "Boot stowage box",
              "Cargo area storage tray",
              "Driver + passenger vanity mirrors",
              "Folding grab handles",
              "Height adjustable front headrests",
              "Height adjustable front seats",
              "Height\\/reach adjust steering wheel",
              "Interior light with delay",
              "Internal chrome door handles",
              "Lower glovebox cover",
              "Luggage load hooks",
              "Pollen filter",
              "Rear storage trays",
              "Rear top tether child seat ISOFIX attachment",
              "Ticket holder",
            ],
            "Driver Convenience": [
              "Exterior temperature gauge",
              "PAS",
              "Service interval indicator",
            ],
            "Engine\\/Drivetrain\\/Suspension": ["Sports suspension"],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00318971",
          tags: [],
          tax_rate_value: null,
          technical_data: {
            cc: {
              name: "CC",
              value: "1198",
              category: "Engine and Drive Train",
            },
            co: {
              name: "CO",
              value: "0.696",
              category: "Emissions - ICE",
            },
            hc: {
              name: "HC",
              value: "0.045",
              category: "Emissions - ICE",
            },
            nox: {
              name: "NOx",
              value: "0.016",
              category: "Emissions - ICE",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            hcnox: {
              name: "HC+NOx",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            width: {
              name: "Width",
              value: "1642",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "Yes",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "128",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1498",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "4000",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "DOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "101",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "3",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "5",
              category: "Weight and Capacities",
            },
            particles: {
              name: "Particles",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            wheelType: {
              name: "Wheel Type",
              value: '15" ALLOY',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2465",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "70",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "SE",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "38.7",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "No",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "ANTARES",
              category: "Tyres",
            },
            maxRoofLoad: {
              name: "Max. Roof Load",
              value: "75",
              category: "Weight and Capacities",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "14.9",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            tyreSizeRear: {
              name: "Tyre Size Rear",
              value: "195\\/55 R15",
              category: "Tyres",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.2",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "51.4",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "51",
              category: "Performance",
            },
            noiseLevelDba: {
              name: "Noise Level dB(A)",
              value: "73",
              category: "Emissions - ICE",
            },
            tyreSizeFront: {
              name: "Tyre Size Front",
              value: "195\\/55 R15",
              category: "Tyres",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "TYRE REPAIR KIT",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "69",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "5400",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "112",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "2",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "12",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "12V",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "76.5",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "62.8",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "11",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "3000",
              category: "Performance",
            },
            compressionRatio: {
              name: "Compression Ratio",
              value: "10.5:1",
              category: "Engine and Drive Train",
            },
            maxLoadingWeight: {
              name: "Max. Loading Weight",
              value: "455",
              category: "Weight and Capacities",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "Not Available",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "86.9",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "83",
              category: "Performance",
            },
            minimumKerbweight: {
              name: "Minimum Kerbweight",
              value: "1095",
              category: "Weight and Capacities",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            grossVehicleWeight: {
              name: "Gross Vehicle Weight",
              value: "1550",
              category: "Weight and Capacities",
            },
            maxTowingWeightBraked: {
              name: "Max. Towing Weight - Braked",
              value: "800",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 5",
              category: "Emissions - ICE",
            },
            widthIncludingMirrors: {
              name: "Width (including mirrors)",
              value: "1886",
              category: "Vehicle Dimensions",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "45",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "315",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "10000",
              category: "General",
            },
            maxTowingWeightUnbraked: {
              name: "Max. Towing Weight - Unbraked",
              value: "500",
              category: "Weight and Capacities",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "10",
              category: "Weight and Capacities",
            },
            heightIncludingRoofRails: {
              name: "Height (including roof rails)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "1180",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "Not Available",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "5E",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "3",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "10",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "308.17",
          vat_scheme: "Margin",
          vat_when_new: "1817.50",
          videos: "[]",
          vin: "TMBFH25J4D3112174",
          vrm: "WJ13EBN",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/skoda-fabia-se-12v-12-12v-se-5dr-00318971",
          year: "2013",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097309\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097309\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097309\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097310\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097310\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097310\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097308\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097308\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097308\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097309\\/skoda-fabia-se-12v-12-12v-se-5dr-00318971-xd6NSZCi.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097310\\/skoda-fabia-se-12v-12-12v-se-5dr-00318971-CKU66vB0.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1097308\\/skoda-fabia-se-12v-12-12v-se-5dr-00318971-UJK8F3C9.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [["MP3", "Aux In", "Isofix"]],
          wheelchair_access: 0,
        },
        {
          advert_classification: "USED",
          advertisable_id: 55018,
          card_guid: 14758,
          admin_fee: "0.00",
          attention_grabber: null,
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "WHITE",
          contents: [],
          company: "Graham Bell Limited",
          date_first_registered: "2014-03-24",
          date_mot_expires: "2022-03-23",
          derivative: "1.2 Pop 3dr",
          description: "",
          doors: "3",
          drivetrain: "Front Wheel Drive",
          engine_size: "1242",
          extra_description: "",
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "6A",
          location: "WSLINE",
          location_slug: "wsline",
          make: "Fiat",
          make_slug: "fiat",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "Punto",
          model_year: null,
          name: "FIAT PUNTO HATCHBACK 1.2 Pop 3dr",
          odometer_units: "Miles",
          odometer_value: 29660,
          original_price: "4999.00",
          plate: "2014 (14)",
          previous_keepers: 0,
          price: "4999.00",
          price_ex_vat: "4999.00",
          price_when_new: "7954.95",
          range: "Punto",
          range_slug: "punto",
          reserved: "Available",
          seats: "5",
          site: "Winsford",
          site_slug: "winsford",
          slug: "fiat-punto-hatchback-12-pop-3dr-00318184",
          standard_equipment: {
            Security: [
              "Immobiliser",
              "Remote central locking",
              "Deadlocks",
              "Lockable fuel cap",
            ],
            Entertainment: [
              "Audio remote control in steering wheel",
              "MP3 compatible radio\\/single CD player",
            ],
            "Passive Safety": [
              "Driver and passenger airbags",
              "ABS\\/EBD",
              "Brake assist function",
              "Tyre pressure monitoring system",
              "Drivers knee airbag",
              "3x3 point rear seatbelts",
              "Window airbags",
              "ESC including ASR\\/MSR + hill hold",
            ],
            "Exterior Features": [
              "Electric front windows",
              "Headlight height adjustment",
              "Body colour door mirrors",
              "Body colour bumpers",
              "Rear window wash\\/wipe",
              "Heated rear windscreen",
            ],
            "Interior Features": [
              "Front headrests",
              "Cloth upholstery",
              "Height adjustable driver's seat",
              "2 rear head restraints",
              "Height\\/reach adjustable steering column",
              "Sunvisor with ticket holder",
            ],
            "Driver Convenience": [
              "Trip computer",
              "Rev counter",
              "Dualdrive PAS",
            ],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00318184",
          tags: [],
          tax_rate_value: "130.00",
          technical_data: {
            cc: {
              name: "CC",
              value: "1242",
              category: "Engine and Drive Train",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            hcnox: {
              name: "HC+NOx",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            width: {
              name: "Width",
              value: "1687",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "No",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "126",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1490",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "4065",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "SOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "97",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "4",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "5",
              category: "Weight and Capacities",
            },
            particles: {
              name: "Particles",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            wheelType: {
              name: "Wheel Type",
              value: '15" STEEL',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2510",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "69",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "Pop",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "39.2",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "No",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "Not Available",
              category: "Tyres",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "14.4",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.2",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "52.3",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "51",
              category: "Performance",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "TYRE REPAIR KIT",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "69",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "5500",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "102",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "3",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "8",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "Not Available",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "70.8",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "64.2",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "10.4",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "3000",
              category: "Performance",
            },
            compressionRatio: {
              name: "Compression Ratio",
              value: "11.0:1",
              category: "Engine and Drive Train",
            },
            maxLoadingWeight: {
              name: "Max. Loading Weight",
              value: "560",
              category: "Weight and Capacities",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "Not Available",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "78.9",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "75",
              category: "Performance",
            },
            minimumKerbweight: {
              name: "Minimum Kerbweight",
              value: "1015",
              category: "Weight and Capacities",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            grossVehicleWeight: {
              name: "Gross Vehicle Weight",
              value: "1575",
              category: "Weight and Capacities",
            },
            maxTowingWeightBraked: {
              name: "Max. Towing Weight - Braked",
              value: "900",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 6",
              category: "Emissions - ICE",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "45",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "275",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "Not Available",
              category: "General",
            },
            maxTowingWeightUnbraked: {
              name: "Max. Towing Weight - Unbraked",
              value: "400",
              category: "Weight and Capacities",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "10.9",
              category: "Weight and Capacities",
            },
            heightIncludingRoofRails: {
              name: "Height (including roof rails)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "1030",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "Not Available",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            timingBeltIntervalMileage: {
              name: "Timing Belt Interval Mileage",
              value: "Not Available",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            serviceIntervalFrequencyMonths: {
              name: "Service Interval Frequency - Months",
              value: "Not Available",
              category: "General",
            },
            timingBeltIntervalFrequencyMonths: {
              name: "Timing Belt Interval Frequency - Months",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "6A",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "3",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "8",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "302.33",
          vat_scheme: "Margin",
          vat_when_new: "1590.99",
          videos: "[]",
          vin: "ZFA1990000P061255",
          vrm: "YD14NPK",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/fiat-punto-hatchback-12-pop-3dr-00318184",
          year: "2014",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088954\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088954\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088954\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088952\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088952\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088952\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088953\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088953\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088953\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088954\\/fiat-punto-hatchback-12-pop-3dr-00318184-BWQShhVh.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088952\\/fiat-punto-hatchback-12-pop-3dr-00318184-ZJk1slUi.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1088953\\/fiat-punto-hatchback-12-pop-3dr-00318184-Bc3BMF5p.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [["MP3"]],
          wheelchair_access: 0,
        },
        {
          advert_classification: "USED",
          advertisable_id: 55534,
          card_guid: 15203,
          admin_fee: "0.00",
          attention_grabber: null,
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "WHITE",
          contents: [],
          company: "Fords Cheshire Limited",
          date_first_registered: "2014-09-23",
          date_mot_expires: "2021-09-22",
          derivative: "1.2 Pop 3dr [Start Stop]",
          description: "",
          doors: "3",
          drivetrain: "Front Wheel Drive",
          engine_size: "1242",
          extra_description: "",
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "9U",
          location: "WSLINE",
          location_slug: "wsline",
          make: "Fiat",
          make_slug: "fiat",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "500",
          model_year: null,
          name: "FIAT 500 HATCHBACK 1.2 Pop 3dr [Start Stop]",
          odometer_units: "Miles",
          odometer_value: 19580,
          original_price: "5099.00",
          plate: "2014 (64)",
          previous_keepers: 2,
          price: "5099.00",
          price_ex_vat: "5099.00",
          price_when_new: "8179.17",
          range: "500",
          range_slug: "500",
          reserved: "Available",
          seats: "4",
          site: "Winsford",
          site_slug: "winsford",
          slug: "fiat-500-hatchback-12-pop-3dr-start-stop-00318685",
          standard_equipment: {
            Security: ["Remote central locking", "Locking fuel filler cap"],
            Entertainment: ["MP3 compatible radio\\/single CD player"],
            "Passive Safety": [
              "Driver and passenger airbags",
              "Side airbags",
              "ABS\\/EBD",
              "Tyre pressure monitoring system",
              "Drivers knee airbag",
              "ESP + ASR\\/MSR + HBA + Hill holder",
              "Window airbags",
            ],
            "Exterior Features": [
              "Electric front windows",
              "Body colour bumpers",
              "Heat insulated glass",
              "Chrome door handles",
              "Heated rear windows with wash wipe",
            ],
            "Interior Features": [
              "Front passenger seat memory",
              "Height adjustable steering wheel",
              "Front headrests",
              "4 speed ventilation system\\/recirculating mode",
              "1 passenger grab handle",
              "Auxilliary 12V power socket",
              "Isofix child seat preparation",
              "Pop cloth upholstery",
            ],
            "Driver Convenience": ["Dualdrive PAS"],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00318685",
          tags: [],
          tax_rate_value: "30.00",
          technical_data: {
            cc: {
              name: "CC",
              value: "1242",
              category: "Engine and Drive Train",
            },
            co: {
              name: "CO",
              value: "0.351",
              category: "Emissions - ICE",
            },
            hc: {
              name: "HC",
              value: "0.042",
              category: "Emissions - ICE",
            },
            nox: {
              name: "NOx",
              value: "0.032",
              category: "Emissions - ICE",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            hcnox: {
              name: "HC+NOx",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            width: {
              name: "Width",
              value: "1627",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "No",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "113",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1488",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "3546",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "SOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "99",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "4",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "4",
              category: "Weight and Capacities",
            },
            particles: {
              name: "Particles",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            wheelType: {
              name: "Wheel Type",
              value: '14" STEEL',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2300",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "69",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "Pop",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "51.4",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "Yes",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "Not Available",
              category: "Tyres",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "12.9",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            tyreSizeRear: {
              name: "Tyre Size Rear",
              value: "175\\/65 R14",
              category: "Tyres",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.2",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "60.1",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "51",
              category: "Performance",
            },
            noiseLevelDba: {
              name: "Noise Level dB(A)",
              value: "73.5",
              category: "Emissions - ICE",
            },
            tyreSizeFront: {
              name: "Tyre Size Front",
              value: "175\\/65 R14",
              category: "Tyres",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "SPACE SAVER",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "69",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "5500",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "102",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "2",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "8",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "Start Stop",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "70.8",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "65.7",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "10.4",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "3000",
              category: "Performance",
            },
            insuranceGroup1: {
              name: "Insurance Group 1",
              value: "03",
              category: "General",
            },
            insuranceGroup2: {
              name: "Insurance Group 2",
              value: "U",
              category: "General",
            },
            compressionRatio: {
              name: "Compression Ratio",
              value: "11.1:1",
              category: "Engine and Drive Train",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "Not Available",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "78.9",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "75",
              category: "Performance",
            },
            minimumKerbweight: {
              name: "Minimum Kerbweight",
              value: "865",
              category: "Weight and Capacities",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            maxTowingWeightBraked: {
              name: "Max. Towing Weight - Braked",
              value: "800",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 6",
              category: "Emissions - ICE",
            },
            widthIncludingMirrors: {
              name: "Width (including mirrors)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "35",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "185",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "18000",
              category: "General",
            },
            maxTowingWeightUnbraked: {
              name: "Max. Towing Weight - Unbraked",
              value: "400",
              category: "Weight and Capacities",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "9.3",
              category: "Weight and Capacities",
            },
            heightIncludingRoofRails: {
              name: "Height (including roof rails)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "550",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "Not Available",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            timingBeltIntervalMileage: {
              name: "Timing Belt Interval Mileage",
              value: "Not Available",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "Not Available",
              category: "General",
            },
            serviceIntervalFrequencyMonths: {
              name: "Service Interval Frequency - Months",
              value: "Not Available",
              category: "General",
            },
            euroNcapPedestrianTestStarRating: {
              name: "EURO NCAP Pedestrian test - Star Rating.",
              value: "N\\/A",
              category: "General",
            },
            timingBeltIntervalFrequencyMonths: {
              name: "Timing Belt Interval Frequency - Months",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "9U",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "3",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            euroNcapFrontAndSideImpactTestStarRating: {
              name: "EURO NCAP Front and Side Impact test - Star Rating.",
              value: "N\\/A",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "8",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "186.77",
          vat_scheme: "Margin",
          vat_when_new: "1635.83",
          videos: "[]",
          vin: "ZFA3120000J228711",
          vrm: "AY64NNG",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/fiat-500-hatchback-12-pop-3dr-start-stop-00318685",
          year: "2014",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096676\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096676\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096676\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096673\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096673\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096673\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096674\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096674\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096674\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096676\\/fiat-500-hatchback-12-pop-3dr-start-stop-00318685-nWcTWdM7.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096673\\/fiat-500-hatchback-12-pop-3dr-start-stop-00318685-awVSyU7i.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1096674\\/fiat-500-hatchback-12-pop-3dr-start-stop-00318685-QdYwyRWc.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [["MP3", "Isofix"]],
          wheelchair_access: 0,
        },
        {
          advert_classification: "USED",
          advertisable_id: 55580,
          card_guid: 15247,
          admin_fee: "0.00",
          attention_grabber: null,
          body_type: "Hatchback",
          body_type_slug: "hatchback",
          co2: "",
          mpg: "",
          cap_database: "CAR",
          "coin-series": "",
          colour: "GREEN",
          contents: [],
          company: "Fords Cheshire Limited",
          date_first_registered: "2012-06-25",
          date_mot_expires: "2022-03-01",
          derivative: "1.2 SZ4 5dr",
          description: "",
          doors: "5",
          drivetrain: "Front Wheel Drive",
          engine_size: "1242",
          extra_description: "",
          fuel_type: "Petrol",
          fuel_type_slug: "petrol",
          insurance_group: "11E",
          location: "WSLINE",
          location_slug: "wsline",
          make: "Suzuki",
          make_slug: "suzuki",
          manufacturer_colour: null,
          meta_description: "",
          meta_keywords: "",
          meta_title: "",
          model: "Swift",
          model_year: null,
          name: "SUZUKI SWIFT HATCHBACK 1.2 SZ4 5dr",
          odometer_units: "Miles",
          odometer_value: 38400,
          original_price: "5299.00",
          plate: "2012 (12)",
          previous_keepers: 1,
          price: "5299.00",
          price_ex_vat: "5299.00",
          price_when_new: "11192.13",
          range: "Swift",
          range_slug: "swift",
          reserved: "Available",
          seats: "5",
          site: "Winsford",
          site_slug: "winsford",
          slug: "suzuki-swift-sz4-12-sz4-5dr-00318730",
          standard_equipment: {
            Wheels: ['16" alloy wheels'],
            Security: ["Deadlocks", "Immobiliser", "Remote central locking"],
            Entertainment: [
              "6 speakers",
              "Bluetooth audio streaming",
              "Radio\\/CD + MP3",
              "USB interface",
            ],
            "Passive Safety": [
              "5 x 3 point seatbelts",
              "ABS+EBD+Brake assist",
              "Curtain airbags",
              "Driver airbag",
              "Driver seatbelt warning indicator",
              "Drivers knee airbag",
              "ESP + traction control",
              "Front passenger airbag deactivation",
              "Front seatbelt pretensioners with force limiters",
              "Height adjustable front seatbelts",
              "Passenger airbag",
              "Passenger seatbelt warning indicator",
              "Rear child proof door locks",
              "Side airbags",
              "Side impact protection beams",
            ],
            "Exterior Features": [
              "2 speed wipers+intermittent wipe",
              "Automatic headlights",
              "Body colour door mirrors and handles",
              "Body coloured bumpers",
              "Electric door mirrors",
              "Electric front windows + drivers one touch",
              "Electric rear windows",
              "Front fog lights",
              "Headlamp levelling",
              "Heated door mirrors",
              "LED daytime running lights",
              "Rear privacy glass",
              "Rear wiper",
              "Tinted glass",
            ],
            "Interior Features": [
              "3 cupholders",
              "3 spoke leather covered steering wheel",
              "60\\/40 split rear seats",
              "Accessory socket",
              "Centre console storage",
              "Climate control",
              "Cloth seat trim",
              "Door pockets with bottle holder",
              "Driver\\/passenger sunvisors with ticket holders + vanity mirrors",
              "Front head restraints",
              "Front map light",
              "Front\\/rear assist grips",
              "Glovebox",
              "Height adjustable driver's seat",
              "Isofix",
              "Luggage area lamp",
              "Passenger seat back pocket",
              "Pollen filter",
              "Rear headrests",
              "Steering wheel audio controls",
              "Storage area with lid",
              "Tilt\\/telescopic adjust steering wheel",
              "Top tether anchor plate for isofix child seat",
            ],
            "Driver Convenience": [
              "Bluetooth hands free telephone connection",
              "Cruise control",
              "Door ajar warning lamp",
              "Fuel consumption screen",
              "Lights on warning",
              "Low fuel level warning light",
              "Outside temperature display",
              "PAS",
              "Remote fuel cap release",
              "Tachometer",
              "Trip computer",
            ],
          },
          status: "FOR_SALE_RETAIL",
          stock_id: "00318730",
          tags: [],
          tax_rate_value: "145.00",
          technical_data: {
            cc: {
              name: "CC",
              value: "1242",
              category: "Engine and Drive Train",
            },
            co: {
              name: "CO",
              value: "0.491",
              category: "Emissions - ICE",
            },
            hc: {
              name: "HC",
              value: "0.044",
              category: "Emissions - ICE",
            },
            nox: {
              name: "NOx",
              value: "0.018",
              category: "Emissions - ICE",
            },
            gears: {
              name: "Gears",
              value: "5 SPEED",
              category: "Engine and Drive Train",
            },
            hcnox: {
              name: "HC+NOx",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            width: {
              name: "Width",
              value: "1695",
              category: "Vehicle Dimensions",
            },
            alloys: {
              name: "Alloys?",
              value: "Yes",
              category: "Tyres",
            },
            co2Gkm: {
              name: "CO2 (g\\/km)",
              value: "116",
              category: "Emissions - ICE",
            },
            height: {
              name: "Height",
              value: "1510",
              category: "Vehicle Dimensions",
            },
            length: {
              name: "Length",
              value: "3850",
              category: "Vehicle Dimensions",
            },
            camshaft: {
              name: "Camshaft",
              value: "DOHC",
              category: "Engine and Drive Train",
            },
            topSpeed: {
              name: "Top Speed",
              value: "103",
              category: "Performance",
            },
            basedOnId: {
              name: "Based On ID",
              value: "Not Available",
              category: "General",
            },
            cylinders: {
              name: "Cylinders",
              value: "4",
              category: "Engine and Drive Train",
            },
            noOfSeats: {
              name: "No. of Seats",
              value: "5",
              category: "Weight and Capacities",
            },
            particles: {
              name: "Particles",
              value: "Not Available",
              category: "Emissions - ICE",
            },
            wheelType: {
              name: "Wheel Type",
              value: '16" ALLOY',
              category: "Tyres",
            },
            wheelbase: {
              name: "Wheelbase",
              value: "2430",
              category: "Vehicle Dimensions",
            },
            badgePower: {
              name: "Badge Power",
              value: "94",
              category: "General",
            },
            coinSeries: {
              name: "Coin Series",
              value: "SZ4",
              category: "General",
            },
            ecUrbanMpg: {
              name: "EC Urban (mpg)",
              value: "46.3",
              category: "Fuel Consumption - ICE",
            },
            spaceSaver: {
              name: "Space Saver?",
              value: "Yes",
              category: "Tyres",
            },
            wheelStyle: {
              name: "Wheel Style",
              value: "Not Available",
              category: "Tyres",
            },
            "0To62MphSecs": {
              name: "0 to 62 mph (secs)",
              value: "12.3",
              category: "Performance",
            },
            engineLayout: {
              name: "Engine Layout",
              value: "FRONT TRANSVERSE",
              category: "Engine and Drive Train",
            },
            fuelDelivery: {
              name: "Fuel Delivery",
              value: "MULTI POINT FUEL INJECTION",
              category: "Engine and Drive Train",
            },
            specialOrder: {
              name: "Special Order",
              value: "No",
              category: "General",
            },
            transmission: {
              name: "Transmission",
              value: "MANUAL",
              category: "Engine and Drive Train",
            },
            tyreSizeRear: {
              name: "Tyre Size Rear",
              value: "185\\/55 R16",
              category: "Tyres",
            },
            badgeEngineCc: {
              name: "Badge Engine CC",
              value: "1.2",
              category: "General",
            },
            ecCombinedMpg: {
              name: "EC Combined (mpg)",
              value: "56.5",
              category: "Fuel Consumption - ICE",
            },
            enginePowerKw: {
              name: "Engine Power - KW",
              value: "69",
              category: "Performance",
            },
            noiseLevelDba: {
              name: "Noise Level dB(A)",
              value: "71",
              category: "Emissions - ICE",
            },
            tyreSizeFront: {
              name: "Tyre Size Front",
              value: "185\\/55 R16",
              category: "Tyres",
            },
            tyreSizeSpare: {
              name: "Tyre Size Spare",
              value: "SPACE SAVER",
              category: "Tyres",
            },
            cylinderLayout: {
              name: "Cylinder Layout",
              value: "IN-LINE",
              category: "Engine and Drive Train",
            },
            enginePowerBhp: {
              name: "Engine Power - BHP",
              value: "94",
              category: "Performance",
            },
            enginePowerRpm: {
              name: "Engine Power - RPM",
              value: "6000",
              category: "Performance",
            },
            engineTorqueNm: {
              name: "Engine Torque - NM",
              value: "118",
              category: "Performance",
            },
            generationMark: {
              name: "Generation Mark",
              value: "3",
              category: "General",
            },
            numberOfValves: {
              name: "Number of Valves",
              value: "16",
              category: "Engine and Drive Train",
            },
            specialEdition: {
              name: "Special Edition",
              value: "No",
              category: "General",
            },
            coinDescription: {
              name: "Coin Description",
              value: "Not Available",
              category: "General",
            },
            cylindersBoreMm: {
              name: "Cylinders - Bore (mm)",
              value: "73",
              category: "Engine and Drive Train",
            },
            ecExtraUrbanMpg: {
              name: "EC Extra Urban (mpg)",
              value: "64.2",
              category: "Fuel Consumption - ICE",
            },
            engineTorqueMkg: {
              name: "Engine Torque - MKG",
              value: "12",
              category: "Performance",
            },
            engineTorqueRpm: {
              name: "Engine Torque - RPM",
              value: "4800",
              category: "Performance",
            },
            compressionRatio: {
              name: "Compression Ratio",
              value: "11:1",
              category: "Engine and Drive Train",
            },
            maxLoadingWeight: {
              name: "Max. Loading Weight",
              value: "460",
              category: "Weight and Capacities",
            },
            ncapSafetyAssist: {
              name: "NCAP Safety Assist %",
              value: "71",
              category: "General",
            },
            cylindersStrokeMm: {
              name: "Cylinders - Stroke (mm)",
              value: "74.2",
              category: "Engine and Drive Train",
            },
            engineTorqueLbsft: {
              name: "Engine Torque - LBS.FT",
              value: "87",
              category: "Performance",
            },
            minimumKerbweight: {
              name: "Minimum Kerbweight",
              value: "1020",
              category: "Weight and Capacities",
            },
            catalyticConvertor: {
              name: "Catalytic Convertor",
              value: "Yes",
              category: "Engine and Drive Train",
            },
            grossVehicleWeight: {
              name: "Gross Vehicle Weight",
              value: "1480",
              category: "Weight and Capacities",
            },
            maxTowingWeightBraked: {
              name: "Max. Towing Weight - Braked",
              value: "1000",
              category: "Weight and Capacities",
            },
            standardEuroEmissions: {
              name: "Standard Euro Emissions",
              value: "EURO 5",
              category: "Emissions - ICE",
            },
            widthIncludingMirrors: {
              name: "Width (including mirrors)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            fuelTankCapacityLitres: {
              name: "Fuel Tank Capacity (Litres)",
              value: "42",
              category: "Weight and Capacities",
            },
            luggageCapacitySeatsUp: {
              name: "Luggage Capacity (Seats Up)",
              value: "211",
              category: "Weight and Capacities",
            },
            serviceIntervalMileage: {
              name: "Service Interval Mileage",
              value: "9000",
              category: "General",
            },
            maxTowingWeightUnbraked: {
              name: "Max. Towing Weight - Unbraked",
              value: "400",
              category: "Weight and Capacities",
            },
            turningCircleKerbToKerb: {
              name: "Turning Circle - Kerb to Kerb",
              value: "10.4",
              category: "Weight and Capacities",
            },
            heightIncludingRoofRails: {
              name: "Height (including roof rails)",
              value: "Not Available",
              category: "Vehicle Dimensions",
            },
            luggageCapacitySeatsDown: {
              name: "Luggage Capacity (Seats Down)",
              value: "528",
              category: "Weight and Capacities",
            },
            ncapPedestrianProtection: {
              name: "NCAP Pedestrian Protection %",
              value: "62",
              category: "General",
            },
            vehicleHomologationClass: {
              name: "Vehicle Homologation Class",
              value: "M1",
              category: "General",
            },
            alternativeFuelQualifying: {
              name: "Alternative Fuel Qualifying",
              value: "No",
              category: "General",
            },
            timingBeltIntervalMileage: {
              name: "Timing Belt Interval Mileage",
              value: "Not Available",
              category: "General",
            },
            ecDirective1999100ecApplies: {
              name: "EC Directive 1999\\/100\\/EC Applies",
              value: "Yes",
              category: "Fuel Consumption - ICE",
            },
            ncapAdultOccupantProtection: {
              name: "NCAP Adult Occupant Protection %",
              value: "94",
              category: "General",
            },
            ncapChildOccupantProtection: {
              name: "NCAP Child Occupant Protection %",
              value: "82",
              category: "General",
            },
            timingBeltIntervalFrequencyMonths: {
              name: "Timing Belt Interval Frequency - Months",
              value: "Not Available",
              category: "General",
            },
            standardManufacturersWarrantyYears: {
              name: "Standard manufacturers warranty - Years",
              value: "3",
              category: "General",
            },
            insuranceGroup150EffectiveJanuary07: {
              name: "Insurance Group 1 - 50 Effective January 07",
              value: "11E",
              category: "General",
            },
            manufacturersPaintworkGuaranteeYears: {
              name: "Manufacturers Paintwork Guarantee - Years",
              value: "Not Available",
              category: "General",
            },
            ncapOverallRatingEffectiveFebruary09: {
              name: "NCAP Overall Rating - Effective February 09",
              value: "5",
              category: "General",
            },
            standardManufacturersWarrantyMileage: {
              name: "Standard manufacturers warranty - Mileage",
              value: "60000",
              category: "General",
            },
            manufacturersCorrosionPerforationGuaranteeYears: {
              name: "Manufacturers Corrosion Perforation Guarantee - Years",
              value: "12",
              category: "General",
            },
            didAtLeastOneAspectOfThisVehiclesSafetyGiveCauseForConcern: {
              name: "Did at least one aspect of this vehicle's safety give cause for concern?",
              value: "No",
              category: "General",
            },
          },
          transmission: "MANUAL",
          vat: "333.17",
          vat_scheme: "Margin",
          vat_when_new: "2238.43",
          videos: "[]",
          vin: "TSMNZC72S00291687",
          vrm: "DA12WPR",
          website_url:
            "https:\\/\\/www.fow.co.uk\\/vehicle\\/used\\/suzuki-swift-sz4-12-sz4-5dr-00318730",
          year: "2012",
          media_urls: [
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094092\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094092\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094092\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094093\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094093\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094093\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094091\\/conversions\\/large.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094091\\/conversions\\/thumb.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094091\\/conversions\\/medium.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            },
            {
              large:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              thumb:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
              medium:
                "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
            },
          ],
          original_media_urls: [
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094092\\/suzuki-swift-sz4-12-sz4-5dr-00318730-84ochkle.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094093\\/suzuki-swift-sz4-12-sz4-5dr-00318730-nMf2v4MG.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/1094091\\/suzuki-swift-sz4-12-sz4-5dr-00318730-eO87wJQV.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/reserve.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/hasslefree.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/adminfees.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/partex.jpg",
            "https:\\/\\/apex4-production.s3.eu-west-1.amazonaws.com\\/tenant_c6c1a765-8ab5-439e-bae5-1df553fe98e8\\/media\\/uploads\\/banners\\/2018\\/finance.jpg",
          ],
          finance: null,
          monthly_payment: null,
          feature_classification: [
            [
              "Bluetooth",
              "Cruise Control",
              "MP3",
              "Automatic Headlights",
              "AC\\/Climate",
              "Isofix",
              "Alloys",
            ],
          ],
          wheelchair_access: 0,
        },
      ],
    };
  },
};
</script>