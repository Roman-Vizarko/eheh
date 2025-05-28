def show_menu
  puts "1. Додавання"
  puts "2. Віднімання"
  puts "3. Множення"
  puts "4. Ділення"
  puts "5. Вихід"
end

def get_input(prompt)
  print prompt
  gets.chomp.to_f
end

loop do
  show_menu
  print "Оберіть операцію (1-5): "
  choice = gets.chomp

  break if choice == "5"

  num1 = get_input("Введіть перше число: ")
  num2 = get_input("Введіть друге число: ")

  case choice
  when "1"
    puts "Результат: #{num1 + num2}"
  when "2"
    puts "Результат: #{num1 - num2}"
  when "3"
    puts "Результат: #{num1 * num2}"
  when "4"
    if num2 == 0
      puts "Помилка: ділення на нуль!"
    else
      puts "Результат: #{num1 / num2}"
    end
  else
    puts "Невірний вибір"
  end

  puts
end

