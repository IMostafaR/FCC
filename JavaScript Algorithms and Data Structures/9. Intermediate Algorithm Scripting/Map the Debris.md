# Map the Debris

According to Kepler's Third Law, the orbital period $T$ of two point masses orbiting each other in a circular or elliptic orbit is:

$$
T = 2\pi \sqrt{\frac{a^3}{\mu}}
$$

- $a$ is the orbit's semi-major axis
- $μ=GM$ is the standard gravitational parameter
- $G$ is the gravitational constant,
- $M$ is the mass of the more massive body.

Return a new array that transforms the elements' average altitude into their orbital periods (in seconds).

The array will contain objects in the format `{name: 'name', avgAlt: avgAlt}`.

The values should be rounded to the nearest whole number. The body being orbited is Earth.

The radius of the earth is $6367.4447$ kilometers, and the $GM$ value of earth is $398600.4418  km^3s^{-2}$.

```js
function orbitalPeriod(arr) {
  const GM = 398600.4418;
  const earthRadius = 6367.4447;
  return arr;
}

orbitalPeriod([{ name: "sputnik", avgAlt: 35873.5553 }]);
```

### Answer

```js
function orbitalPeriod(arr) {
  const GM = 398600.4418;
  const earthRadius = 6367.4447;

  function calculateOrbitalPeriod(avgAlt) {
    const a = earthRadius + avgAlt;
    const T = 2 * Math.PI * Math.sqrt(Math.pow(a, 3) / GM);
    return Math.round(T);
  }

  const result = [];

  for (let i = 0; i < arr.length; i++) {
    const { name, avgAlt } = arr[i];
    const orbitalPeriod = calculateOrbitalPeriod(avgAlt);
    result.push({ name, orbitalPeriod });
  }

  return result;
}

orbitalPeriod([{ name: "sputnik", avgAlt: 35873.5553 }]);
```
