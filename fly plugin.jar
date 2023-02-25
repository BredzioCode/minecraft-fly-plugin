package com.example.fly;

import org.bukkit.command.Command;
import org.bukkit.command.CommandSender;
import org.bukkit.entity.Player;
import org.bukkit.plugin.java.JavaPlugin;

public class FlyPlugin extends JavaPlugin {

    @Override
    public void onEnable() {
        // Plugin enabled
        getLogger().info("Fly plugin enabled!");
    }

    @Override
    public void onDisable() {
        // Plugin disabled
        getLogger().info("Fly plugin disabled!");
    }

    @Override
    public boolean onCommand(CommandSender sender, Command cmd, String label, String[] args) {
        if (cmd.getName().equalsIgnoreCase("fly")) {
            if (!(sender instanceof Player)) {
                sender.sendMessage("This command can only be executed by a player.");
                return true;
            }
            Player player = (Player) sender;
            if (player.getAllowFlight()) {
                player.setAllowFlight(false);
                player.sendMessage("Flying has been disabled.");
            } else {
                player.setAllowFlight(true);
                player.sendMessage("Flying has been enabled.");
            }
            return true;
        }
        return false;
    }
}
