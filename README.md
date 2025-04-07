# OOP-assignment.-Py
# Creating a Flower class, representing a general flower with its characteristics
class Flower:
    def __init__(self, color, species, fragrance, height):
        # Attributes that define each flower
        self.color = color          # The color of the flower (e.g., 'red', 'yellow')
        self.species = species      # The species of the flower (e.g., 'Rose', 'Tulip')
        self.fragrance = fragrance  # The fragrance the flower emits (e.g., 'sweet', 'strong')
        self.height = height        # Height of the flower in centimeters

    # Method to simulate the flower blooming
    def bloom(self):
        print(f"The {self.species} flower with {self.color} petals is blooming and spreading its {self.fragrance} fragrance!")

    # Method to display information about the flower
    def display_info(self):
        print(f"Flower Details:")
        print(f"Species: {self.species}")
        print(f"Color: {self.color}")
        print(f"Fragrance: {self.fragrance}")
        print(f"Height: {self.height} cm")

# Creating an object of the Flower class
flower1 = Flower("Red", "Rose", "sweet", 50)
flower1.display_info()  # Display the flower's details
flower1.bloom()  # Simulate the flower blooming

# Now, let's create a subclass for Roses, which will inherit from Flower

class Rose(Flower):
    def __init__(self, color, fragrance, height, thorniness):
        super().__init__(color, "Rose", fragrance, height)  # Call the parent class constructor with Rose-specific info
        self.thorniness = thorniness  # Extra attribute specific to Roses

    # Override the bloom method to make the Rose unique
    def bloom(self):
        print(f"The {self.color} Rose is blooming with a {self.thorniness} level of thorns, emitting a {self.fragrance} fragrance!")

# Create an object of the Rose class
rose1 = Rose("Pink", "strong", 60, "high")
rose1.display_info()  # Display Rose-specific info
rose1.bloom()  # Simulate the Rose blooming
