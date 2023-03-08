This repo is here to prove that the implicit dependencies override as described [here](https://nx.dev/reference/project-configuration#implicitdependencies) doesn't work.
Screenshot of docs:
![Screenshot 2023-03-08 at 11 09 44](https://user-images.githubusercontent.com/23667517/223671021-df3c1c43-97ad-402c-82c0-247d736b84f3.png)


In the [project.json](https://github.com/rdenner/nx-implicit-dependencies-broken/blob/main/packages/is-odd/project.json#L6) of `is-odd` a rule has been added to negate the dependency with `is-even`, but this is still the graph:

![Screenshot 2023-03-08 at 11 10 38](https://user-images.githubusercontent.com/23667517/223671206-28c8cbc7-73e3-4a26-83af-99b7226dab2f.png)

![graph](https://user-images.githubusercontent.com/23667517/223670090-5058ac4f-8413-4bf8-98b6-a50020738626.png)

This functionality did work in nx 15.0.3.
