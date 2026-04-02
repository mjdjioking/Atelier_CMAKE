# On active les fonctionnalités de test
enable_testing()

# On définit le test nommé "TestCarre"
# COMMAND définit l'exécutable à lancer et ses arguments
add_test(NAME TestCarre COMMAND calculator car 5)

# On définit le résultat attendu (Expression régulière)
# Puisque vous utilisez %lf dans le printf, le résultat sera 25.000000
set_tests_properties(TestCarre PROPERTIES PASS_REGULAR_EXPRESSION "25\\.0+")
