Feature: Potion of Size Change

  Scenario Outline: Drinking the Potion of Size Change
    Given a <creature_size> creature drinks the Potion of Size Change
    When 2 hours have passed
    Then the creature's size is changed to <new_size>
    And after 2 hours, the creature's size is reverted back to <creature_size>

    Examples:
      | creature_size | new_size |
      | tiny          | normal   |
      | normal        | large    |
      | large         | huge     |
      | huge          | tiny     |

