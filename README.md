Your-First-Step
YOUR FIRST STEP: ----------------------------------------------------------------- A Web based sharing of Geo-Information in regard to solve the initial problems of newcomer international student in Karlsruhe Concept: As there are many reputed educational institute like KIT, HSKA situated in Karlsruhe, so many international students have come in previous years and the numbers are increasing year after year. The main problem has been notice here is insufficient of relevant information in their initiation stage in Karlsruhe. Often it has been asked by international students, that where they find a room in Karlsruhe or Rothaus or Mensa? And how they could reach their? Definitely Studentwerk, ASTA etc. are available to help those students, but the fact is most of them do not know where exactly the Studentwerk or ASTA offices are actually situated. So when they come here for study they should have an idea about their first few steps before beginning their Study. The main goal of this project is to provide a dynamic web based solution of those problems. So that every student could understand and able to go through their initiation stage in Karlsruhe by their own. And that is why the name of this project is ‚YOUR FIRST STEP‘. Target Group: All newcomer international students in Karlsruhe. Area of Interest Karlsruhe, Germany Developer: ------------------------------------------------------------- Md. Shamimul Islam Fickrie Muhammad Murshed Alam All are MSc. Students in International Masters Geomatics, University of Applied Science Karlsruhe, Germany. How to load: ------------------------------------------------------------ Client Side: - Clone this repository into your local - Copy the yourfirststep folder in to your c:\xampp\htdox\xampp drive - Then the index.php file will be visible in the browser http://localhost/xampp/yourfirststep (but in server side a database is must to get all function active: see server side part) - Now you can edit or develop more on it to improve the application. - HTML5 use to develop the web page, Java Script is use to display the map and PHP use to connect the database with website and for query. - For individual service page code will found in service folder. Connection: - config.php file has been created to make the connection. Connection parameters are server name, user name and password like "localhost","root","" and database name is "your_firststep". " $connect = mysql_connect("localhost","root","") or die("Couldn't connect with Database. Please, try again!"); mysql_select_db("your_firststep") or die("Couldn't find this Database!"); " Server Side: - Install XAMPP if you do not have one (https://www.apachefriends.org/de/download.html) - Create a database with a name your_firststep and import the your_firststep.sql file in side the Database folder, this database is connected via php with the website to display and store comments of the clients - PostgreSQL database hosting different tables that store geometry data (‘features’) corresponding to the different ‘layers’ that are displayed in the ‘pgrouting' client - pgRouting extension that has been added (by default) to PostgreSQL database. The ‘ways’ table is pgRouting geometry (the_geom) enabled which is returned to the client application (‘Your First Step') via GeoServer - GeoServer is the WMS service provider. It exposes the different PostgreSQL tables to the ‘Your First Step' application via webservice calls via http://localhost:8082 Data Preparing: - The geo data can be downloaded from OSM Metro Extracts (http://mapzen.com/metro-extracts/) - PostGIS use to import osm2pgrouting - Add your layers to your PostGIS database - Publish layers from the PostGIS database on Geoserver - Create a workspace called "pgrouting" - Create a store called "pgrouting" PgRouting: Following steps have to follow to provide routing facilities to the cling. For more information you can use the following web links. http://download.osgeo.org/pgrouting/foss4g2010/workshop/docs/pgRoutingWorkshop.pdf http://workshop.pgrouting.org/chapters/php_server.html - Create database "routing" in PostgreSQL - Add postgis and pgRouting extension to the database (see workshop chapter 3.3) (-- add PostGIS functions CREATE EXTENSION postgis; -- add pgRouting core functions CREATE EXTENSION pgrouting;) - Create a connection between this database and QGIS (Add PostGIS Table in QGIS) - Follow the further instructions in the PgRouting workshop from FOSS4G (http://workshop.pgrouting.org/chapters/topology.html) with chapter 4 (Create a Network Topology) and chapter 5 (PgRouting Algorithms) - test the routable database (ways layer) with QGis by using pgrouting layer extension Final Output: www.your-firststep.de Contract: ------------------------------------------------------ For any kinds of further question, interest, problem or discussion please contract with - Md. Shamimul Islam - rubel_ku03@yahoo.com (www.rubelshorizon.com) Fickrie Muhammad - fickrie.muhammad@yahoo.com 
