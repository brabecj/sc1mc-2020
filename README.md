# sc1mc-2022
SC1MC-2022 Database
The datbase includes sets of di-, tetra-, and octa- artificial molecular complexes. Molecules have been built by combining seven atoms (Cr, Mn, Fe, Co, Ni, Cu, Zn) as cores and nine ligands (Br–, Cl–, F–, S2–, NH3, CO,H2O, NC–, N(CH)5) as surrounders. Ligands are placed at three different distances from core, and no more than two different ligands are allowed within one compound. Electronic structures for all complexes have been solved at Hartree-Fock level with NWChem ab initio software package and Ahlrichs pVDZ basis set. For each complex an active space of 36 orbitals has been defined. Entropies have been estimated with MOLMPS program using 1024 bond dimesion in 16 sweeps.

JSON structure

    "Abbreviation"                  - the abbraviation of the molecular complex, string
    "Atoms"                         - list of atoms
            "aid"                   - numerical identifier for atoms, list of integers, size of the list is equal to the number of atoms
            "element"               - labels of atomic species, list of strings, size of the list is equal to the number of atoms
    "Coords"                        - Cartesian coordinates of atoms, list of three-dimensional vectors with floats, size of the list is equal to the number of atoms
    "NOrbs"                         - number of molecular orbitals in active space, integer
    "NActElec"                      - number of active electrons, integer
    "TotalSCFEn"                    - total Hartree-Fock energy, float
    "NucRepEn"                      - nuclear-nuclear repulsion energy, float
    "CoreEn"                        - core energy, float
    "Orbitals"                      - molecular orbital's info
            "number"                - the formal number of the orbital in the active space, integer
            "energy"                - Hartree-Fock orbital energy, float
            "occupation"            - occupation number of the orbital, float
            "r^2"                   - spacial extention of the orbital, float
            "bondchar"              - bonding/antibonding character of the orbital, integer
            "vector"                - list of atomic orbitals, that construct the molecular orbital
                    "aid"           - identifier of the atom, integer
                    "element"       - label of atom specie, string
                    "coeff"         - expansion coefficient, float
                    "shell"         - atomic orbital shell, integer
                    "func"          - atomic orbital type, string
            "1orb_ent"              - single-orbital entropy, float
            "2orb_ent"              - two-orbital entropies between the orbital and all other orbitals in active space for the molecule, list of floats
    "Integrals"                     - multicenter one- and two-electron integrals
            "1electron"             - multiceter one-electron integrals
                    "orb1"          - the identifier for first orbital in integral, integer
                    "orb2"          - the identifier for second orbital in integral, integer
                    "value"         - value of the integral, float
            "2electronC"            - multicenter Coulomb integrals
                    "orb1"          - the identifier for first orbital in integral, integer
                    "orb2"          - the identifier for second orbital in integral, integer
                    "value"         - value of the integral, float
            "2electronE"            - multicenter exchange integrals
                    "orb1"          - the identifier for first orbital in integral, integer
                    "orb2"          - the identifier for second orbital in integral, integer
                    "value"         - value of the integral, float
