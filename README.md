# Number-of-Pets
def main():
    file = open("n_pets (1).tx","r")
    total_families = 0
    total_pets = 0
    Maximum = 0
    Minimum = 10

    for line in file:
        total_families = total_families + 1
        total_pets = int(line) + total_pets
        if int(line) > Maximum:
            Maximum = int(line)
        if int(line) < Minimum:
            Minimum = int(line)
    Average = total_pets / total_families

    print("Total Number of families: ",total_families)
    print("Total number of pets: ",total_pets)
    print("Average number of pets per family: ",Average)
    print("Maximum number of pets in a family: ",Maximum)
    print("Minimum number of pets in a family: ",Minimum)

    r = open("results.txt","w")

    r.write("Total Number of families: "+str(total_families))

    r.write("\nTotal number of pets: "+str(total_pets))
  
    r.write("\nAverage number of pets per family: "+str(Average))
  
    r.write("\nMaximum number of pets in a family: "+str(Maximum))
    
    r.write("\nMinimum number of pets in a family: "+str(Minimum))

    file.close()
    r.close()

main()
