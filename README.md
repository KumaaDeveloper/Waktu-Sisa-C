# General
Simple pocktmine code for gamemode
  
## Code
```php
<?php

namespace KumaDev\SimpleGamemode;

use pocketmine\plugin\PluginBase;
use pocketmine\command\Command;
use pocketmine\command\CommandSender;
use pocketmine\player\Player;
use pocketmine\player\GameMode;

class Main extends PluginBase {
    public function onEnable(): void {
        $this->getLogger()->info("Plugin Telah Aktif");
    }

    public function onCommand(CommandSender $sender, Command $command, string $label, array $args): bool
    {
        if (!sender instanceof Player) return false;

        switch ($label) {
            case "gma":
                $sender->setGamemode(GameMode::ADVENTURE());
                $sender->sendMessage("Mode Game Anda Sekarang Adalah Adventure");
                break;
            case "gmc":
                $sender->setGamemode(GameMode::CREATIVE());
                $sender->sendMessage("Mode Game Anda Sekarang Adalah Creative");
                break;
            case "gms":
                $sender->setGamemode(GameMode::SURVIVAL());
                $sender->sendMessage("Mode Game Anda Sekarang Adalah Survival");
                break;
            case "gmspc":
                $sender->setGamemode(GameMode::SPECTATOR());
                $sender->sendMessage("Mode Game Anda Sekarang Adalah Spectator");
                break;
            default:
                return false;    
        }

        return true;
    }
}
```
