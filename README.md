# Corpse
[![](https://jitpack.io/v/unldenis/Corpse.svg)](https://jitpack.io/#unldenis/Corpse)<br>
Dead bodies in minecraft for 1.8-1.20.x servers.
## Installation
1. Put the jar in the plugins folder.
2. Reboot your server. Do not use /reload
## Developer Api
```java
public class CorpseAPI {

  /**
   * Class method that allows you to use the API.
   *
   * @return an instance of this class
   */
  @NotNull
  public static synchronized CorpseAPI getInstance();

  /**
   * Method that creates a corpse in the player's position and with its skin and inventory
   *
   * @return a new Corpse object
   */
  public Corpse spawnCorpse(@NotNull Player player);

  /**
   * Method that creates a corpse in the given place and with the skin, name and inventory of the
   * player
   *
   * @param location The location where to spawn the corpse
   * @return a new Corpse object
   */
  public Corpse spawnCorpse(@NotNull Player player, @NotNull Location location);

  /**
   * Method that creates a corpse in the given place and with the skin and name of the
   * offlinePlayer
   *
   * @param location      The location where to spawn the corpse
   * @return a new Corpse object
   */
  public Corpse spawnCorpse(@NotNull OfflinePlayer offlinePlayer, @NotNull Location location);

  /**
   * Method that creates a corpse in the given place and with the skin and name of the player with a
   * custom inventory.
   *
   * @param location   The location where to spawn the corpse
   * @param helmet     The helmet to put on the corpse
   * @param chestPlate The chestPlate to put on the corpse
   * @param leggings   The leggings to put on the corpse
   * @param boots      The boots to put on the corpse
   * @return a new Corpse object
   */
  public Corpse spawnCorpse(
      @NotNull Player player,
      @NotNull Location location,
      @Nullable ItemStack helmet,
      @Nullable ItemStack chestPlate,
      @Nullable ItemStack leggings,
      @Nullable ItemStack boots
  );

  /**
   * Method that creates a corpse in the given place and with the skin and name of the offlinePlayer
   * with a custom inventory.
   *
   * @param location      The location where to spawn the corpse
   * @param helmet        The helmet to put on the corpse
   * @param chestPlate    The chestPlate to put on the corpse
   * @param leggings      The leggings to put on the corpse
   * @param boots         The boots to put on the corpse
   * @return a new Corpse object
   */
  public Corpse spawnCorpse(
      @NotNull OfflinePlayer offlinePlayer,
      @NotNull Location location,
      @Nullable ItemStack helmet,
      @Nullable ItemStack chestPlate,
      @Nullable ItemStack leggings,
      @Nullable ItemStack boots
  );

  /**
   * Method that removes a corpse
   *
   * @param corpse The corpse to be removed
   */
  public void removeCorpse(@NotNull Corpse corpse);
}

```
