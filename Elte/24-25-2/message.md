# Safari Játék Specifikációk

## Bevezetés

A dokumentum ezen a része a Safari játék funkcionális
és nem funkcionális specifikációit tartalmazza. A játék egy 2D felülnézetes szimuláció,
amelyben a játékosok egy afrikai szafariparkot menedzselnek.
A játék magában foglalja a vadon élő állatok kezelését, a turizmust és a gazdaságot.

## Funkcionális Követelmények

### Játékmenet

**Időkezelés**:
A játékosok különböző idősebességek között válthatnak (óra/nap/hét) a játék során.
**Terep Elemei**:
A térkép növényeket, vízfelületeket és ösvényeket tartalmaz,
amelyeket módosítani lehet.
**Vadvilág Szimuláció**:
A ragadozók és növényevők együtt élnek, élelemre és vízre van szükségük,
öregszenek, és természetes viselkedéseket mutatnak, mint például a vándorlás
és a szaporodás.
**Turista Interakció**:
A turisták meglátogatják a szafarit, dzsipeket bérelnek, és befolyásolják
a park bevételeit.
**Gazdasági Rendszer**:
A játékosok erőforrásokat kezelnek állatok, járművek és infrastruktúra adásvételével.
**Győzelmi feltétel**:
A játék véget ér, ha lejárt az idő és a küszöbérték felett van az állatpopuláció,
és a pénzmennyiség.
**Vereségi feltétel**:
Az állat populáció küszöbérték alá megy, vagy kifogyott a játékos a pénzből.

### Játék Komponensek

**Minitérkép**:
Egy navigálható minitérkép segíti a játékosokat a nagyobb játéktér
megtekintésében és kezelésében.
**2.5D Grafika**:
Az objektumok vizuálisan átfedik egymást egy pszeudo-3D hatás érdekében.
**Procedurális Térkép Generálás**:
A kezdeti térkép Perlin Noise segítségével generálódik.
**Környezeti Akadályok**:
A dombok és folyók befolyásolják a mozgást és a láthatóságot.
**Játékállapot Mentése**:
A játékosok elmenthetik és betölthetik a haladásukat.

## Nem Funkcionális Követelmények

### Technikai Specifikációk

**Programozási Nyelv**:
Python
**Játékmotor**:
Pygame a megjelenítéshez és a bevitelkezeléshez
**Entitás Rendszer**:
Az Esper ECS keretrendszert használja a moduláris entitás viselkedéshez

### Teljesítmény & Használhatóság

**Zökkenőmentes Játékmenet**: A játéknak stabil képfrissítési rátával kell futnia.
**Skálázhatóság**: A kódbázisnak támogatnia kell a jövőbeli bővítéseket.
**Felhasználói Élmény**: Intuitív UI és vezérlők a gördülékeny élmény érdekében.
