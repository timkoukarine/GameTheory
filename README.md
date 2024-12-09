## Simple Game Theory Solver for Two Player Games with Incomplete Information

This module allows the user to solve for nash equilibrium in both perfect and inperfect information games involving 2 players.

It is intended to be run in an interactive window.
Running gto.py will preinitialize a game with 4 subgames and random payoffs for testing.

Otherwise games can be initialized and will ask for user input.

### Running the module.

game = Game(num_subgames: int, A1: tuple[str], A2: tuple[str], NumT1: int, NumT2: int)

game.build_subgames0(subgames: list[pd.DataFrame]) -> will ask for inputs for payoffs in each field for each player

game.set_game_weights(game_weights: list[Fraction]) -> will ask for game probabilities (numerator, then denominator)

game.get_weighted_payoffs() - No Input Needed

game.set_weighted_types(weighted_types: dict[tuple[int, int], pd.DataFrame]) -> Will ask for each player's realized type vector for each game

game.build_strategic_form() - No Input Needed

game.find_nash() -> will return pure nash equilibrium strategy profiles (if found)

check any game properties with:
game.subgames

game.strategic_game

game.{property... etc.}
