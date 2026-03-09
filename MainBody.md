<!DOCTYPE html>
<html>
<head>
	<title>BotW Guide Login</title>
	<style>
		body {
			min-height: 100vh;
			margin: 0;
			display: flex;
			flex-direction: column;
			font-family: sans-serif;
			background-color: #ffffff;
		}
		#register-form {
			background-color: #464646;
			align-items: center;
			padding: 2rem;
			border-radius: 12px;
			width: 280px;
			text-align: center;
			display: none;
			color: #d7fff4;
		}
		#login-form {
			background-color: #464646;
			padding: 2rem;
			border-radius: 12px;
			width: 280px;
			text-align: center;
			display: none;
			align-items: center;
			color: #d7fff4;
		}
		h1 {
			margin-bottom: 1rem;
			letter-spacing: 2px;
		}
		input {
			width: 100%;
			padding: 10px;
			margin: 0.5rem 0;
			border: none;
			border-radius: 6px;
			background: #0e4b47;
			color: #d7fff4;
		}
		button {
			width: 100%;
			padding: 10px;
			margin-top: 1rem;
			background: #2fffd5;
			color: #003330;
			font: bold;
		}
		button:hover {
			background: #8ffff0;
		}
		.msg {
			font-size: 0.85rem;
			color: #ffbdbd;
		}
        #menu {
            background-color: #464646;
            color: #d7fff4;
            border-radius: 12px;
            padding: 2rem;
            width: 320px;
            max-width: 90%;
            text-align: center;
            box-shadow: 0 4px 16px rgba(0,0,0,0.15);
            margin-bottom: 2rem;
            display: none;
        }
		#menus {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			justify-content: center;
		}
		#content {
			position: absolute;
			top: 0;
			left: 50%;
			transform: translateX(-50%);
			width: auto;
			display: flex;
			flex-direction: column;
			align-items: center;
			margin-top: 0;
		}
		#cookingHeader {
			background-color: #464646;
			padding: 2rem;
			text-align: center;
			color: #d7fff4;
			letter-spacing: 2px;
		}
		#cookingWrapper {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 2rem;
		}
		#cookingIntro,
		#healingMeals,
		#buffMeals,
		#resistanceMeals,
		#elixirsSection,
		#advancedCooking,
		#ingredientTips {
			background-color: #464646;
			padding: 2rem;
			border-radius: 12px;
			width: 600px;
			max-width: 90%;
			margin-bottom: 2rem;
			color: #d7fff4;
		}
		#cookingFooter {
			background-color: #464646;
			text-align: center;
			padding: 1rem;
			color: #d7fff4;
		}
		#combatHeader {
			background-color: #464646;
			padding: 2rem;
			text-align: center;
			color: #d7fff4;
			letter-spacing: 2px;
		}
		#combatWrapper {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 2rem;
		}
		#combatCard1,
		#combatCard2,
		#combatCard3,
		#combatCard4,
		#combatCard5 {
			background-color: #464646;
			padding: 2rem;
			border-radius: 12px;
			width: 600px;
			max-width: 90%;
			margin-bottom: 2rem;
			color: #d7fff4;
		}
		#combatFooter {
			background-color: #464646;
			text-align: center;
			padding: 1rem;
			color: #d7fff4;
		}
		#beastHeader {
			background-color: #464646;
			padding: 2rem;
			text-align: center;
			color: #d7fff4;
			letter-spacing: 2px;
		}
		#beastWrapper {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 2rem;
		}
		#beastIntro,
		#rutaSection,
		#rudaniaSection,
		#medohSection,
		#naborisSection,
		#blightBosses {
			background-color: #464646;
			padding: 2rem;
			border-radius: 12px;
			width: 600px;
			max-width: 90%;
			margin-bottom: 2rem;
			color: #d7fff4;
		}
		#beastFooter {
			background-color: #464646;
			text-align: center;
			padding: 1rem;
			color: #d7fff4;
		}
		#shrineHeader {
			background-color: #464646;
			padding: 2rem;
			text-align: center;
			color: #d7fff4;
			letter-spacing: 2px;
		}
		#shrineWrapper {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 2rem;
		}
		#shrineIntro,
		#puzzleShrines,
		#combatShrines,
		#blessingShrines,
		#apparatusShrines,
		#shrineRewards,
		#advancedStrategies {
			background-color: #464646;
			padding: 2rem;
			border-radius: 12px;
			width: 600px;
			max-width: 90%;
			margin-bottom: 2rem;
			color: #d7fff4;
			margin-top: 2rem;
		}
		#shrineFooter {
			background-color: #464646;
			text-align: center;
			padding: 1rem;
			color: #d7fff4;
		}
		#ganonHeader {
			background-color: #464646;
			padding: 2rem;
			text-align: center;
			color: #d7fff4;
			letter-spacing: 2px;
		}
		#ganonWrapper {
			flex: 1;
			display: flex;
			flex-direction: column;
			align-items: center;
			padding: 2rem;
		}
		#castleSection,
		#preparationSection,
		#calamitySection,
		#darkBeastSection,
		#completionSection {
			background-color: #464646;
			padding: 2rem;
			border-radius: 12px;
			width: 600px;
			max-width: 90%;
			margin-bottom: 2rem;
			color: #d7fff4;
		}
		#ganonFooter {
			background-color: #464646;
			text-align: center;
			padding: 1rem;
			color: #d7fff4;
		}
		#Thing1 {
			display: none;
		}
		#Thing2 {
			display: none;
		}
		#Thing3 {
			display: none;
		}
		#Thing4 {
			display: none;
		}
		#Thing5 {
			display: none;
		}
		#returnMenu {
			display: none;
			padding: 20px;
		}
	</style>
</head>
<body>
	<div id="menus">
		<form id="register-form">
			<h1>BotW Guide Register</h1>
			<input id="user-register" placeholder="Traveler Name">
			<input id="pass-register" type="password" placeholder="Sheikah Slate Key">
			<button type="submit">Enter Hyrule</button>
			<div class="msg-register" id="msg-register"></div>
			<button onclick="ermLogin()"> Login Here </button>
		</form>
		<form id="login-form">
			<h1>BotW Guide Login</h1>
			<input id="user-login" placeholder="Traveler Name" required>
			<input id="pass-login" type="password" placeholder="Sheikah Slate Key" required>
			<button type="submit">Enter Hyrule</button>
			<div class="msg-login" id="msg-login"></div>
		</form>
		<div id="menu" class="menu">
			<h1> Welcome to Hyrule! </h1>
			<h4> Please pick which topic you wish to learn about! </h4>
			<ul>
				<li> <button onclick="Thing(1);"> Cooking </button> </li>
				<li> <button onclick="Thing(2);"> Combat </button> </li>
				<li> <button onclick="Thing(3);"> Divine beasts </button> </li>
				<li> <button onclick="Thing(4);"> Shrines </button> </li>
				<li> <button onclick="Thing(5);"> Final Battle </button> </li>
				<li> <button onclick="logout();"> Logout </button> </li>
				<li> <button onclick="unregister();"> Unregister </button> </li>
			</ul>
		</div>
	</div>
	<div id="content">
		<div id="returnMenu">
			<button onclick="showMenu()">Return To Menu</button>
		</div>
		<div id="Thing1">
			<header id="cookingHeader">
				<h1>Breath of the Wild Guide</h1>
				<p>Page 1 — Complete Cooking & Elixirs Guide</p>
			</header>
			<section id="cookingWrapper">
				<div id="cookingIntro">
					<h2>How Cooking Works</h2>
					<p>
						Cooking is essential for survival in Hyrule.
						Combine up to five ingredients in a cooking pot to create meals
						that restore health and grant special effects.
					</p>
					<ul>
						<li>More ingredients = stronger effects</li>
						<li>Mix similar effects for better bonuses</li>
						<li>Avoid mixing different buff types</li>
						<li>Cooking during a Blood Moon increases critical chance</li>
					</ul>
				</div>
				<div id="healingMeals">
					<h2>Healing Meals</h2>
					<ul>
						<li>Apples and mushrooms restore small health</li>
						<li>Raw meat restores moderate health</li>
						<li>Hearty ingredients fully restore hearts</li>
						<li>Hearty meals grant temporary bonus hearts</li>
					</ul>
					<p>
						Hearty Radishes and Hearty Durians are among the strongest
						healing ingredients in the game.
					</p>
				</div>
				<div id="buffMeals">
					<h2>Attack & Defense Buffs</h2>
					<ul>
						<li>Mighty ingredients boost attack power</li>
						<li>Tough ingredients boost defense</li>
						<li>Razorclaw Crab increases attack</li>
						<li>Fortified Pumpkin increases defense</li>
					</ul>
					<p>
						Buff strength depends on ingredient quantity and quality.
						Maximum buff level is 3.
					</p>
				</div>
				<div id="resistanceMeals">
					<h2>Environmental Resistance</h2>
					<ul>
						<li>Spicy ingredients provide cold resistance</li>
						<li>Chillshrooms provide heat resistance</li>
						<li>Electro ingredients resist lightning</li>
						<li>Fireproof lizards prevent burning on Death Mountain</li>
					</ul>
					<p>
						Resistance duration increases with more ingredients of the same type.
					</p>
				</div>
				<div id="elixirsSection">
					<h2>Elixirs</h2>
					<p>
						Elixirs require one critter and at least one monster part.
					</p>
					<ul>
						<li>Hightail Lizard + Bokoblin Horn = Speed Elixir</li>
						<li>Fireproof Lizard + Moblin Fang = Fireproof Elixir</li>
						<li>Restless Cricket + Monster Part = Stamina Elixir</li>
					</ul>
					<p>
						Stronger monster parts increase duration.
					</p>
				</div>
				<div id="advancedCooking">
					<h2>Advanced Cooking Tips</h2>
					<ul>
						<li>Use 5 of the same buff ingredient for maximum effect</li>
						<li>Cook just before tough boss fights</li>
						<li>Sell high-value meals for rupees</li>
						<li>Use stamina meals before long climbs</li>
						<li>Prep shock resistance before fighting Thunderblight</li>
					</ul>
				</div>
				<div id="ingredientTips">
					<h2>Ingredient Farming Tips</h2>
					<ul>
						<li>Hunt animals in cold regions for prime meat</li>
						<li>Gather mushrooms near forests and caves</li>
						<li>Fish near Zora's Domain for quality seafood</li>
						<li>Farm Hearty Durians in Faron region</li>
					</ul>
					<p>
						Always restock before entering major dungeons.
					</p>
				</div>
			</section>
			<footer id="cookingFooter">
				<p>Page 1 of the Breath of the Wild Strategy Guide</p>
			</footer>
		</div>
		<div id="Thing2">
			<header id="combatHeader">
				<h1>Breath of the Wild Guide</h1>
				<p>Page 2 — Complete Combat Guide</p>
			</header>
			<section id="combatWrapper">
				<div id="combatCard1">
					<h2>Basic Combat Controls</h2>
					<ul>
						<li>Y Button – Standard Attack</li>
						<li>Hold Y – Charged Attack</li>
						<li>ZL – Shield Guard</li>
						<li>X – Jump</li>
						<li>ZR – Bow</li>
					</ul>
					<p>Mastering movement and timing is more important than raw weapon strength.</p>
				</div>
				<div id="combatCard2">
					<h2>Perfect Dodge & Flurry Rush</h2>
					<p>
						A Perfect Dodge is performed by jumping sideways or backward at the
						last moment before an enemy attack lands.
					</p>
					<ul>
						<li>Side hop for horizontal attacks</li>
						<li>Backflip for vertical attacks</li>
						<li>Triggers slow motion</li>
						<li>Allows multiple rapid strikes</li>
					</ul>
					<p>Flurry Rush is one of the most powerful mechanics in the game.</p>
				</div>
				<div id="combatCard3">
					<h2>Shield Parry</h2>
					<p>
						Press A while guarding to perform a shield parry.
						This can deflect projectiles and even Guardian laser beams.
					</p>
					<ul>
						<li>Timing is critical</li>
						<li>Prevents shield durability loss when perfect</li>
						<li>Essential for advanced Guardian fights</li>
					</ul>
				</div>
				<div id="combatCard4">
					<h2>Enemy Types & Strategies</h2>
					<ul>
						<li><strong>Bokoblins</strong> – Basic enemies, vulnerable to headshots</li>
						<li><strong>Moblin</strong> – Stronger, slower attacks</li>
						<li><strong>Lizalfos</strong> – Fast and evasive</li>
						<li><strong>Hinox</strong> – Giant cyclops, attack the eye</li>
						<li><strong>Guardian</strong> – Use Ancient weapons or parry lasers</li>
					</ul>
					<p>Always assess enemy weapons before engaging.</p>
				</div>
				<div id="combatCard5">
					<h2>Advanced Combat Tips</h2>
					<ul>
						<li>Use the environment (exploding barrels, cliffs)</li>
						<li>Lightning during storms affects metal gear</li>
						<li>Fire spreads through grass for updrafts</li>
						<li>Elemental arrows deal bonus effects</li>
						<li>Stealth strikes deal massive damage</li>
					</ul>
					<p>
						Creative use of physics often wins battles faster than brute force.
					</p>
				</div>
			</section>
			<footer id="combatFooter">
				<p>Page 2 of the Breath of the Wild Strategy Guide</p>
			</footer>
		</div>
		<div id="Thing3">
			<header id="beastHeader">
				<h1>Breath of the Wild Guide</h1>
				<p>Page 3 — Divine Beasts Complete Strategy</p>
			</header>
			<section id="beastWrapper">
				<div id="beastIntro">
					<h2>Overview of the Divine Beasts</h2>
					<p>
						The four Divine Beasts are massive mechanical constructs built to defeat Calamity Ganon.
						Each functions as a dungeon and ends with a Blight Ganon boss fight.
					</p>
					<ul>
						<li>Free the Champion spirit</li>
						<li>Gain a powerful Champion ability</li>
						<li>Weaken Ganon at Hyrule Castle</li>
					</ul>
				</div>
				<div id="rutaSection">
					<h2>Divine Beast Vah Ruta</h2>
					<p><strong>Region:</strong> Zora's Domain</p>
					<p><strong>Ability Gained:</strong> Mipha's Grace (automatic revival)</p>
					<ul>
						<li>Use Cryonis to solve water puzzles</li>
						<li>Rotate the trunk to redirect water flow</li>
						<li>Activate five terminals</li>
					</ul>
					<p>
						Boss: Waterblight Ganon — Use arrows during spear throws and Cryonis
						to block ice attacks.
					</p>
				</div>
				<div id="rudaniaSection">
					<h2>Divine Beast Vah Rudania</h2>
					<p><strong>Region:</strong> Death Mountain</p>
					<p><strong>Ability Gained:</strong> Daruk's Protection (auto shield)</p>
					<ul>
						<li>Navigates in darkness initially</li>
						<li>Use bombs to clear obstacles</li>
						<li>Manipulate the Beast’s rotation</li>
					</ul>
					<p>
						Boss: Fireblight Ganon — Use bombs when shielded and ice weapons
						for elemental advantage.
					</p>
				</div>
				<div id="medohSection">
					<h2>Divine Beast Vah Medoh</h2>
					<p><strong>Region:</strong> Rito Village</p>
					<p><strong>Ability Gained:</strong> Revali's Gale (vertical wind boost)</p>
					<ul>
						<li>Use updrafts for aerial combat</li>
						<li>Tilt the Beast to access terminals</li>
						<li>Archery skill is critical</li>
					</ul>
					<p>
						Boss: Windblight Ganon — Maintain distance and use slow-motion bow shots.
					</p>
				</div>
				<div id="naborisSection">
					<h2>Divine Beast Vah Naboris</h2>
					<p><strong>Region:</strong> Gerudo Desert</p>
					<p><strong>Ability Gained:</strong> Urbosa's Fury (area lightning attack)</p>
					<ul>
						<li>Complex rotating cylinder puzzles</li>
						<li>Electric-based mechanisms</li>
						<li>Most difficult Beast for many players</li>
					</ul>
					<p>
						Boss: Thunderblight Ganon — Extremely fast.
						Perfect dodge is highly recommended.
					</p>
				</div>
				<div id="blightBosses">
					<h2>Blight Ganon Battle Tips</h2>
					<ul>
						<li>Prepare elemental resistance meals</li>
						<li>Upgrade armor before attempting</li>
						<li>Bring multiple weapon types</li>
						<li>Master Flurry Rush timing</li>
					</ul>
					<p>
						Completing all four Divine Beasts significantly weakens the final battle.
					</p>
				</div>
			</section>
			<footer id="beastFooter">
				<p>Page 3 of the Breath of the Wild Strategy Guide</p>
			</footer>
		</div>
		<div id="Thing4">
			<section id="shrineWrapper">
				<header id="shrineHeader">
					<h1>Breath of the Wild Guide</h1>
					<p>Page 4 — Complete Shrines Guide</p>
				</header>
				<div id="shrineIntro">
					<h2>Overview of Shrines</h2>
					<p>
						There are over 100 Shrines scattered across Hyrule.
						Each Shrine rewards a Spirit Orb upon completion.
					</p>
					<ul>
						<li>4 Spirit Orbs = 1 Heart Container or Stamina Vessel</li>
						<li>Fast travel points</li>
						<li>Contain treasure chests</li>
					</ul>
				</div>
				<div id="puzzleShrines">
					<h2>Puzzle Shrines</h2>
					<p>
						These focus on environmental logic and Sheikah Slate abilities.
					</p>
					<ul>
						<li>Magnesis metal object manipulation</li>
						<li>Cryonis ice pillar creation</li>
						<li>Stasis momentum puzzles</li>
						<li>Remote Bomb physics challenges</li>
					</ul>
					<p>
						Observation is key. Look for patterns, switches, and movable structures.
					</p>
				</div>
				<div id="combatShrines">
					<h2>Combat Trial Shrines</h2>
					<p>
						These pit you against Guardian Scouts.
					</p>
					<ul>
						<li>Minor Test of Strength</li>
						<li>Modest Test of Strength</li>
						<li>Major Test of Strength</li>
					</ul>
					<p>
						Use perfect dodge and shield parry.
						Ancient weapons are especially effective.
					</p>
				</div>
				<div id="blessingShrines">
					<h2>Blessing Shrines</h2>
					<p>
						These Shrines contain no puzzles or enemies.
						They are unlocked after completing a quest or hidden challenge.
					</p>
					<ul>
						<li>Often tied to Shrine Quests</li>
						<li>May require environmental exploration</li>
						<li>Reward high-value treasure</li>
					</ul>
				</div>
				<div id="apparatusShrines">
					<h2>Apparatus Shrines</h2>
					<p>
						These require motion controls to tilt platforms and guide objects.
					</p>
					<ul>
						<li>Balance metal balls</li>
						<li>Guide spheres through mazes</li>
						<li>Flip platforms creatively</li>
					</ul>
					<p>
						Some players flip the controller upside down for easier control.
					</p>
				</div>
				<div id="shrineRewards">
					<h2>Rewards & Progression</h2>
					<ul>
						<li>Spirit Orbs</li>
						<li>Weapons and shields</li>
						<li>Rare crafting materials</li>
						<li>Elemental gear</li>
					</ul>
					<p>
						Prioritize stamina upgrades early for exploration benefits.
					</p>
				</div>
				<div id="advancedStrategies">
					<h2>Advanced Shrine Strategies</h2>
					<ul>
						<li>Use Stasis on moving platforms to freeze momentum</li>
						<li>Stack objects creatively to bypass puzzles</li>
						<li>Use Revali’s Gale for unintended shortcuts</li>
						<li>Look for hidden treasure chests using Magnesis</li>
					</ul>
					<p>
						Many puzzles have multiple solutions. Creativity is rewarded.
					</p>
				</div>
			</section>
			<footer id="shrineFooter">
				<p>Page 4 of the Breath of the Wild Strategy Guide</p>
			</footer>
		</div>
		<div id="Thing5">
			<header id="ganonHeader">
				<h1>Breath of the Wild Guide</h1>
				<p>Page 5 — Hyrule Castle & Final Battle</p>
			</header>
			<section id="ganonWrapper">
				<div id="castleSection">
					<h2>Entering Hyrule Castle</h2>
					<p>
						Hyrule Castle is the final dungeon area and can be entered at any time.
						The difficulty depends on how many Divine Beasts you have completed.
					</p>
					<ul>
						<li>Multiple entrances (ground, docks, air)</li>
						<li>High-level enemies throughout</li>
						<li>Powerful weapons hidden inside</li>
						<li>Environmental hazards and Guardians</li>
					</ul>
					<p>
						Stealth and preparation are recommended for first-time players.
					</p>
				</div>
				<div id="preparationSection">
					<h2>Recommended Preparation</h2>
					<ul>
						<li>At least 13–15 Hearts (Master Sword requirement)</li>
						<li>Upgraded armor sets</li>
						<li>Ancient or high-damage weapons</li>
						<li>Strong bows and elemental arrows</li>
						<li>Healing meals and defense buffs</li>
					</ul>
					<p>
						Completing all four Divine Beasts removes half of Ganon’s health
						before the battle begins.
					</p>
				</div>
				<div id="calamitySection">
					<h2>Calamity Ganon Battle</h2>
					<p>
						The first phase combines all Blight Ganon attack styles.
					</p>
					<ul>
						<li>Use Flurry Rush frequently</li>
						<li>Parry laser attacks with shield timing</li>
						<li>Use Urbosa’s Fury for heavy damage</li>
						<li>Target weak points when exposed</li>
					</ul>
					<p>
						During phase two, Ganon becomes shielded.
						Use perfect parries or Urbosa’s Fury to break defenses.
					</p>
				</div>
				<div id="darkBeastSection">
					<h2>Dark Beast Ganon</h2>
					<p>
						After defeating Calamity Ganon, the battle moves outside.
						This becomes a large-scale cinematic encounter.
					</p>
					<ul>
						<li>Ride your horse for mobility</li>
						<li>Use the Bow of Light</li>
						<li>Target glowing weak points</li>
						<li>Final shot ends the battle</li>
					</ul>
					<p>
						This fight focuses more on spectacle than difficulty.
					</p>
				</div>
				<div id="completionSection">
					<h2>After the Battle</h2>
					<ul>
						<li>Game reloads before final fight</li>
						<li>Completion star appears on save file</li>
						<li>Map completion percentage unlocked</li>
						<li>Side quests remain available</li>
					</ul>
					<p>
						You can continue exploring Hyrule to reach 100% completion.
					</p>
				</div>
			</section>
			<footer id="ganonFooter">
				<p>Page 5 of the Breath of the Wild Strategy Guide</p>
			</footer>
		</div>
	</div>
	<script>
		function Thing(x) {
			hideThings();
			document.querySelector("#Thing" + x).style.display = "block";
			document.querySelector("#returnMenu").style.display = "inline-block";
			document.querySelector("#menu").style.display = "none";
		}
		function hideThings() {
			let i = 1;
			while (i < 6) {
				document.querySelector("#Thing" + i).style.display = "none";
				i++;
			}
		}
		function showMenu() {
			hideThings();
			document.querySelector("#returnMenu").style.display = "none";
			document.querySelector("#menu").style.display = "inline-block";
		}
		function ermLogin() {
			document.querySelector("#register-form").style.display = "none";
			document.querySelector("#login-form").style.display = "inline-block";
		}
		function checkPassword(ul, pl) {
			return localStorage.getItem("username") == ul && localStorage.getItem("password") == pl;
		}
		function showMsgRegister(m) {
			const msg = document.getElementById("msg-register");
			msg.textContent = m;
		}
		function showMsgLogin(m) {
			const msg = document.getElementById("msg-login");
			msg.textContent = m;
		}
		function login() {
			const ul = document.querySelector("#user-login").value;
			const pl = document.querySelector("#pass-login").value;
			if (checkPassword(ul, pl)) {
				document.querySelector("#login-form").style.display = "none";
				document.querySelector("#menu").style.display = "inline-block";
				localStorage.setItem("loginSuccessful", true);
			} else {
				showMsgLogin("Sheikah Slate denied. Please enter the correct password.");
			}
		}
		function register() {
			localStorage.setItem("username", document.querySelector("#user-register").value);
			localStorage.setItem("password", document.querySelector("#pass-register").value);
			let un = localStorage.getItem("username");
			let pwd = localStorage.getItem("password")
			showMsgRegister("Sheikah Slate added. Please login with your new password. ");
		}
		const form1 = document.getElementById("login-form");
		const form2 = document.getElementById("register-form");
		form1.addEventListener("submit", function (event) {
			const form1 = document.getElementById("login-form");
			event.preventDefault(); // Prevents the page from reloading
			login();
		});
		form2.addEventListener("submit", function (event) {
			const form2 = document.getElementById("register-form");
			event.preventDefault(); // Prevents the page from reloading
			register();
		});
		window.onload = function () {
			if (localStorage.getItem("username")) {
				if (localStorage.getItem("loginSuccessful")) {
					document.querySelector("#login-form").style.display = "none";
					document.querySelector("#menu").style.display = "inline-block";
					document.querySelector("#register-form").style.display = "none";
				}
				else {
					document.querySelector("#login-form").style.display = "inline-block";
					document.querySelector("#register-form").style.display = "none";
				}
			}
			else {
				document.querySelector("#register-form").style.display = "inline-block";
			}
		};
		function unregister() {
			localStorage.removeItem("username");
			window.location.reload();
		}
		function logout() {
			showMsgLogin("logging out");
			localStorage.removeItem("loginSuccessful");
			window.location.reload();
		}
	</script>
</body>
</html>
