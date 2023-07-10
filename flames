function playFlamesGame(name1, name2) {
  // Step 1: Convert names to lowercase and remove spaces
  name1 = name1.toLowerCase().replace(/\s/g, '');
  name2 = name2.toLowerCase().replace(/\s/g, '');

  // Step 2: Remove common letters
  var letters1 = name1.split('');
  var letters2 = name2.split('');

  for (var i = 0; i < letters1.length; i++) {
    var index = letters2.indexOf(letters1[i]);
    if (index !== -1) {
      letters1.splice(i, 1);
      letters2.splice(index, 1);
      i--;
    }
  }

  // Step 3: Count the remaining letters
  var count = letters1.length + letters2.length;

  // Step 4: Perform the repetitive elimination process
  var flames = ['F', 'L', 'A', 'M', 'E', 'S'];
  var length = flames.length;

  for (var j = 0; j < length - 1; j++) {
    var removeIndex = (count - 1) % flames.length;
    flames.splice(removeIndex, 1);
    flames = flames.concat(flames.splice(0, removeIndex));
    length--;
  }

  // Step 7: Determine the relationship status
  var relationshipStatus = '';

  switch (flames[0]) {
    case 'F':
      relationshipStatus = 'Friends';
      break;
    case 'L':
      relationshipStatus = 'Lovers';
      break;
    case 'A':
      relationshipStatus = 'Affectionate';
      break;
    case 'M':
      relationshipStatus = 'Married';
      break;
    case 'E':
      relationshipStatus = 'Enemies';
      break;
    case 'S':
      relationshipStatus = 'Siblings';
      break;
    default:
      relationshipStatus = 'No relationship found';
      break;
  }

  return relationshipStatus;
}

// Example usage
var player1 = prompt('Enter the name of player 1:');
var player2 = prompt('Enter the name of player 2:');

var result = playFlamesGame(player1, player2);
console.log('Relationship status:', result);
