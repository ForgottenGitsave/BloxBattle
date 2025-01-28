# BloxBattle 
A combo based fighting game made by BadAimStudios/ForgottenStudios


## Features
Multiplayer battles
Combo based attacks
Ai-Battler

## File Structure
	LICENSE
	README.md

	server #Main server hosting filetree (Shipped seperatly)
		src
			__init__.py
			Networking
				Host
					host.py # Allows user connections to device (All world connections)
					subconnect.py # Connect two peers and remove from host server until end of battle (p2p connect)
					server_type.py # Seperate server types (USWest, UK, EU, AUS, etc)
					anticheat.py # Checks and validates files of user and checks for "badpackets (if a script that isnt a game script is running along side of the game/injected into game)"
					report.py # Handles the user reporting system (later update)
			UserDatabase
				Connected
					conencted_users.py
					fighting_users.py
					waiting_or_idle.py
					user_files_update.py
				Offline
					offline_users.json
					last_connection.json
				Banned
					banned_users.json
					ban_user.py
					bantest.py
					autoreban.py
					unban.py

 	player # Main player filetree (packaged into a .zip for players to use)
		src
			__init__.py
			Animations # Animations handler
				__init__.py
				fighting_animations.py
				menu_animations.py
			Scenes # Scenes handler
				__init__.py
				Game # The maps for the gamemodes
					__init__.py
					multiplayer_map.py
					test_your_might.py
					inf1v1.py
					training.py
					debug.py

				Menu # The seperate menus
					__init__.py
					main_menu.py
					settings_menu.py
					credits_menu.py
					multiplayer_server_menu.py
					character_select_multiplayer_menu.py
					character_select_solo.py
			Engine
				__init__.py
				MenuHandler
					__init__.py
					menu_update.py
					interaction_handler.py
				Player
					__init__.py
					combo_handler.py
					input_handler.py
					player_render.py
					player_const.py
					character_handler.py
					colisions_handler.py
					physics_handler.py

 				Ai
					__init__.py
					combo_handler.py
					action_handler.py
					ai_render.py
					ai_const.py
					character_handler.py
					colisions_handler.py
					physics_handler.py
 				Map
					__init__.py
					map_render.py

 			Networking
			(will do it later)
 		
