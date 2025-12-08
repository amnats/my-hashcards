let words = a.new.map(t => t.Value.Vocabulary).slice(1).flatMap(t => t.Items);

words.map(w => ({id: w.Id, word: w.Word, translation: w.Translation }));

console.log(words.reduce((str, curr) => {
    return str + `Q: ${curr.word}\nA: ${curr.translation}\n\n`;
}, ""))
