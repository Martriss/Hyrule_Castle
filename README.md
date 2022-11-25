Projet réalisé dans le cadre de la piscine de l'ETNA.
L'objectif était de créer un RPG en tour par tour dans un délai de 3 jours.
Projet effectué en solo.

Sujet

<html>
<body>
  <div class="panel-heading panel-objective">Objectives</div>
  <div class="panel-body">
    <ul>
      <li>Apply basic TypeScript concepts through a project</li>
      <li>Deal with game development problematics</li>
      <li>Manage user input and its error handling</li>
      <li>Improve your programming knowledge by building a script</li>
      <li>Create gameplay around algorithmic and mathematic functions</li>
    </ul>
  </div>
  <div class="panel-heading panel-project">Instructions</div>
  <div class="panel-body">
    <p>During this project, you will build a little RPG and decide on which game mechanics you wish to implement.</p>
    <p>First, you will have to make the basis of the game. Then, you will be able to pick mods out of a given list. Each
      mod you successfully implement will give you additional points, based on their difficulty.</p>
  </div>
  <div class="panel-heading panel-warning">Before adding mods</div>
  <div class="panel-body">
    <p>Once you are done with the Base Game, you have to put it in a <code>base_game/</code> folder, for correction
      purposes. You can then use a copy of it for the modded game.</p>
    <p>The modded game has to be in a <code>mods/</code> folder and every mod in a different file.</p>
    <p>For instance, if you implement the mods <strong>More Statistics</strong> and <strong>Better Combat
        Options</strong>, we will have inside the <code>mods/</code> folder <code>hyrule_castle.ts</code>,
      <code>more_statistics.ts</code> and <code>better_combat_options.ts</code>.</p>
    <p>Moreover, it is highly recommended to plan ahead and decide how many mods you will implement,
      rather than adding each mod on top of the other.</p>
    <p>Be careful before adding anything not specified in the subject. Any new functionality that is not listed as a
      mod won't earn you any points.</p>
    <p>The only bonuses that will earn you points are a little story or lore and a beautiful and colorful display.</p>
  </div>
  <div class="panel-heading panel-exercise">Step 1: Base Game</div>
  <div class="panel-body">
    <p>Before moving on to the mods, it is mandatory to have the basics of the game.</p>
    <p>The game is a turn-by-turn RPG. You incarnate a character that challenges the Hyrule Castle, a tower composed of
      10 floors. Each floor you encounter an enemy and on the last floor, you challenge the Boss.</p>
    <p>For now, your character will be Link. He has 60 maximum health points (HP) and 15 strength (STR).</p>
    <p>Each fight you will face a Bokoblin which has 30 HP and 5 STR.</p>
    <p>For the 10th floor boss, you will have to defeat “Ganon” who will have 150 HP and 20 STR.</p>
    <p>During each fight, you have the choice between “Attack” and “Heal”:</p>
    <ul>
      <li>“Attack” deals damage to the opponent equal to the <strong>STR</strong> stat of the character</li>
      <li>“Heal” will heal the character by half of his maximum <strong>HP</strong></li>
    </ul>
    <p>After your character's turn, the opponent attacks and deals damage equal to his STR.</p>
    <p>When the opponent's HPs fall to 0, he is defeated and the character climbs one more floor.</p>
    <p>When the character's HPs fall to 0, he dies and the game stops.</p>
    <p>If the boss is defeated, the game stops with a message of congratulations.</p>
  </div>
  <div class="panel-heading panel-info">How to manage a project</div>
  <div class="panel-body">
    <p>For this project, there are many things to do.</p>
    <p>Using a sheet of paper, for instance, try to segment your project in different steps. Make sure everyone in the
      group has an equal amount of work.</p>
    <p>You also need to plan ahead and decide now which mods you want to add to your game.</p>
  </div>
  <div class="panel-heading panel-exercise">Step 2: Dynamic Characters</div>
  <div class="panel-body">
    <p>Using the parsing knowledge you acquired, you will fetch the data of the characters from the given JSON files.
    </p>
    <p>These files are available on your intra:</p>
    <ul>
      <li>The player character will be fetched from the players.json file</li>
      <li>The enemies will be fetched from the enemies.json file</li>
      <li>The boss character will be fetched from the bosses.json file</li>
    </ul>
    <p>The player character, the enemies, and the boss will be randomly selected, using the rarity as a probability
      vector (see Game mechanics &gt; Rarity).</p>
  </div>
  <div class="panel-heading panel-example">Example</div>
  <div class="panel-body">
    <p>You don't have to exactly follow the display of these examples. They're only here to give you some ideas.</p>
    <h3>Combat display</h3><img src="https://i.imgur.com/PODQkck.png" width="60%">
    <img src="https://i.imgur.com/EU2lQzl.png" width="60%">
    <img src="https://i.imgur.com/lhdMPPL.png" width="60%">
    <img src="https://i.imgur.com/oFU2ZlD.png" width="60%">

  </div>
  <div class="panel-heading panel-exercise">Step 3: Mods</div>
  <div class="panel-body">
    <p>Now that you have done the base game and added a bit of dynamism to the characters, let's move on to the mods.
      Your game is boring and unattractive, but with a few tweaks, you can make it much more interesting.</p>
    <p>You can start adding mods to your game. Be careful to respect the prerequisites for each mod, you can't be
      corrected otherwise.</p>
    <p>Every mod explanation is given in the <strong>Better_Combat_Options.html</strong>,
      <strong>Basic_Characteristics.html</strong> and <strong>Basic_Game_Customization.html</strong> files.</p>
    <p>You can do as many mods or mod types you wish as long as you respect the requirements.</p>
    <p>Good luck!</p>
  </div>
  <div class="panel-heading panel-info">Game mechanics</div>
  <div class="panel-body">
    <p><strong>Damage Modifiers</strong></p>
    <p>The Damage Modifiers will be used in the following order.</p>
    <table>
      <thead>
        <tr>
          <th>Modifier</th>
          <th>Formula</th>
          <th>Description</th>
          <th>Example</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>Base damage</td>
          <td>STR</td>
          <td>The base damage is equal to the STR stat</td>
          <td>12</td>
        </tr>
        <tr>
          <td>Critical Strike</td>
          <td>BD × 2</td>
          <td>Double the Base damage</td>
          <td>12 × 2 = 24</td>
        </tr>
        <tr>
          <td>Res/Def</td>
          <td>T - T × (def/100)</td>
          <td>Use of the res or def stats on the total</td>
          <td>24 - 24 × (8/100) = 22.08</td>
        </tr>
        <tr>
          <td>Strength &amp; Weaknesses</td>
          <td>T × 2</td>
          <td>Use of the strength/weaknesses multipliers, from /4 to x4 on the total</td>
          <td>22.08 × 2 = 44.16</td>
        </tr>
        <tr>
          <td>Fear</td>
          <td>T / 2</td>
          <td>Halve the total damage</td>
          <td>44.16 / 2 = 22.08</td>
        </tr>
        <tr>
          <td>Weakening</td>
          <td>T × 1.5</td>
          <td>Add +50% damage on the total damage</td>
          <td>22.08 × 1.5 = 33.12</td>
        </tr>
        <tr>
          <td>Skill “Defend”</td>
          <td>T / 2</td>
          <td>Halve the total damage</td>
          <td>33.12 / 2 = 16.56</td>
        </tr>
      </tbody>
    </table>
    <p>Finally, the total value has to be rounded down to the whole number. Here, 16.56 will be reduced to 16.</p>
    <h3>Rarity</h3>
    <p>Some random events are influenced by rarity. It is the case for player and enemies choice, item drops, etc.
      Rarity is the first value used to calculate the odd of “choosing” an entity or an item.</p>
    <p>For instance, when the player drops an item, first the rarity of the dropped item will be calculated, and then a
      random item from the chosen rarity will be given. The same goes for every enemy encountered or playable character.
    </p>
    <p>Each rarity has different chances to be chosen:</p>
    <table>
      <thead>
        <tr>
          <th>Rarity Tier</th>
          <th>Percentage</th>
          <th>Example</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <td>0</td>
          <td>0%</td>
          <td>Special undropables skill and items</td>
        </tr>
        <tr>
          <td>1</td>
          <td>50%</td>
          <td>Low-level Potion, Skulltula, Link</td>
        </tr>
        <tr>
          <td>2</td>
          <td>30%</td>
          <td>Potion, Lizalfos, Young Link</td>
        </tr>
        <tr>
          <td>3</td>
          <td>15%</td>
          <td>Good Potion, Dead Hand, Sheik</td>
        </tr>
        <tr>
          <td>4</td>
          <td>4%</td>
          <td>High-level Potion, Stalfos, Impa</td>
        </tr>
        <tr>
          <td>5</td>
          <td>1%</td>
          <td>Holy Potion, Guardian, Hylia</td>
        </tr>
      </tbody>
    </table>
  </div>
</body>

</html>
