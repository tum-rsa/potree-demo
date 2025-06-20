# Potree Demo

This is a demo repository of self-hosted 3D Web Viewer by [Potree](https://github.com/potree/potree).


## Data

The demo point clouds should be stored in `.copc.laz` format under `/pointclouds` directory. 

It includes multi-temporal 3D point clouds:

```
Isar_20240812_UPH_10cm.copc.laz
Isar_20241105_UPH_10cm.copc.laz
Isar_20250325_ULS_10cm.copc.laz
```

and bi-temporal surface changes, presented by point cloud distances, i.e., [M3C2 distances](https://py4dgeo.readthedocs.io/en/latest/m3c2.html#References):

```
Isar_m3c2_240812_241105_10cm.copc.laz
Isar_m3c2_240812_250325_10cm.copc.laz
```

## To start the service:

To start a potree viewer, you can use any service supporting static website hosting. Here, we use the [*serve*](https://snapcraft.io/serve) command tool under a linux distribution (e.g., [wsl](https://learn.microsoft.com/en-us/windows/wsl/setup/environment)) and use the below command:
```
serve -p 1234 -d .
```

Then you can visit the local-hosted website and open the potree viewer via the `Isar_Riverbank.html`.

# Reference

- [What is a LAS file?](https://laspy.readthedocs.io/en/latest/intro.html)
- [Cloud Optimized Point Cloud Specification - 1.0](https://copc.io/)
- [Potree](https://github.com/potree/potree)
- [Basic M3C2 algorithm](https://py4dgeo.readthedocs.io/en/latest/m3c2.html)