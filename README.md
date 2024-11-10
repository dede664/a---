# a-et-à
<!DOCTYPE html>
<html lang="fr">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Exercice - a vs à</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
        }

        .correct {
            color: green;
        }

        .incorrect {
            color: red;
        }

        .analyse {
            color: blue;
        }
    </style>
    <script>
        function verifier() {
            let reponsesCorrectes = ["a", "à", "a", "à", "à", "a", "a", "à", "a", "à", 
                                     "a", "à", "à", "a", "a", "à", "a", "à", "a", "à"];
            let score = 0;

            for (let i = 0; i < reponsesCorrectes.length; i++) {
                let userInput = document.getElementById('reponse' + (i + 1)).value.trim().toLowerCase();
                let feedback = document.getElementById('feedback' + (i + 1));
                let analyse = document.getElementById('analyse' + (i + 1));

                if (userInput === reponsesCorrectes[i]) {
                    feedback.innerText = "✔️ Correct";
                    feedback.className = "correct";
                    analyse.innerText = "";
                    score++;
                } else {
                    feedback.innerText = "❌ Incorrect";
                    feedback.className = "incorrect";
                    analyse.innerText = `La bonne réponse est "${reponsesCorrectes[i]}". Rappel : "a" est le verbe avoir conjugué à la troisième personne du singulier (ex : Il a un livre), tandis que "à" est une préposition (ex : Il va à l'école).`;
                    analyse.className = "analyse";
                }
            }

            document.getElementById('score').innerText = `Votre score : ${score}/${reponsesCorrectes.length}`;
        }
    </script>
</head>

<body>
    <h2>Règle : "a" vs "à"</h2>
    <p>
        - <b>"a"</b> est le verbe <i>avoir</i> conjugué à la troisième personne du singulier. Exemple : "Il a un chien".<br>
        - <b>"à"</b> est une préposition, utilisée pour indiquer un lieu, une direction, ou une intention. Exemple : "Elle va à la bibliothèque".
    </p>

    <h2>Exercice - Complétez avec "a" ou "à"</h2>

    <!-- Génération des 20 questions -->
    <div id="exercices">
        <p>1. Il ___ acheté un cadeau.</p>
        <input type="text" id="reponse1"> <span id="feedback1"></span><br>
        <p id="analyse1"></p><br>

        <p>2. Elle part ___ la plage.</p>
        <input type="text" id="reponse2"> <span id="feedback2"></span><br>
        <p id="analyse2"></p><br>

        <p>3. Marie ___ une nouvelle voiture.</p>
        <input type="text" id="reponse3"> <span id="feedback3"></span><br>
        <p id="analyse3"></p><br>

        <p>4. Il est allé ___ Paris.</p>
        <input type="text" id="reponse4"> <span id="feedback4"></span><br>
        <p id="analyse4"></p><br>

        <p>5. Je vais ___ l'école tous les jours.</p>
        <input type="text" id="reponse5"> <span id="feedback5"></span><br>
        <p id="analyse5"></p><br>

        <p>6. Paul ___ fini ses devoirs.</p>
        <input type="text" id="reponse6"> <span id="feedback6"></span><br>
        <p id="analyse6"></p><br>

        <p>7. Elle ___ une belle robe.</p>
        <input type="text" id="reponse7"> <span id="feedback7"></span><br>
        <p id="analyse7"></p><br>

        <p>8. Le chat est ___ côté du canapé.</p>
        <input type="text" id="reponse8"> <span id="feedback8"></span><br>
        <p id="analyse8"></p><br>

        <p>9. Il ___ une idée géniale.</p>
        <input type="text" id="reponse9"> <span id="feedback9"></span><br>
        <p id="analyse9"></p><br>

        <p>10. Ils se dirigent ___ la gare.</p>
        <input type="text" id="reponse10"> <span id="feedback10"></span><br>
        <p id="analyse10"></p><br>

        <p>11. Pierre ___ un frère.</p>
        <input type="text" id="reponse11"> <span id="feedback11"></span><br>
        <p id="analyse11"></p><br>

        <p>12. Il va ___ la piscine demain.</p>
        <input type="text" id="reponse12"> <span id="feedback12"></span><br>
        <p id="analyse12"></p><br>

        <p>13. Elle part ___ 14 heures.</p>
        <input type="text" id="reponse13"> <span id="feedback13"></span><br>
        <p id="analyse13"></p><br>

        <p>14. Elle ___ beaucoup de travail.</p>
        <input type="text" id="reponse14"> <span id="feedback14"></span><br>
        <p id="analyse14"></p><br>

        <p>15. Il ___ trouvé son chemin.</p>
        <input type="text" id="reponse15"> <span id="feedback15"></span><br>
        <p id="analyse15"></p><br>

        <p>16. Ils arrivent ___ la maison à midi.</p>
        <input type="text" id="reponse16"> <span id="feedback16"></span><br>
        <p id="analyse16"></p><br>

        <p>17. Jean ___ un bon livre.</p>
        <input type="text" id="reponse17"> <span id="feedback17"></span><br>
        <p id="analyse17"></p><br>

        <p>18. Elle est ___ la montagne.</p>
        <input type="text" id="reponse18"> <span id="feedback18"></span><br>
        <p id="analyse18"></p><br>

        <p>19. Il ___ perdu ses clés.</p>
        <input type="text" id="reponse19"> <span id="feedback19"></span><br>
        <p id="analyse19"></p><br>

        <p>20. Ils vont ___ une fête ce soir.</p>
        <input type="text" id="reponse20"> <span id="feedback20"></span><br>
        <p id="analyse20"></p><br>
    </div>

    <button onclick="verifier()">Vérifier</button>
    <p id="score"></p>
</body>

</html>
