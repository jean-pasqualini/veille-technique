# Comment implémenter un cerle d'amis

### Qui sont les utilisateurs ?

jean est une personne et a un cercle d'amis
philippe est une personne et a un cercle d'amis

### Par qui ma objet (voiture) est visible ?

jean a une voiture rouge est visible par son cercle d'amis
philippe a une voiture bleu est visible par son cercle d'amis

### Dans quel cerle est-on ?

jean est dans le cercle d'amis de philippe
phille n'est pas dans le cercle d'amis de jean

### Qui peut voir quoi ?

jean peut voir la voiture bleu de philipe et sa propre voiture rouge
philipe peut voir sa voiture bleu mais ne peut pas voir la voiture rouge de jean

### Et en terme d'utilisateur ?

je selectionne la voiture bleu bleu de philippe et recupere son cercle d'amis
j'y trouve jean et philippe

je selectionne la voiture rouge de jean et recupere son cercle d'amis
j'y trouve jean

### Donc

Pour cela il faut bien que jean et philippe ait deux groupe distinct

Un cercle est comme une relation qui peut être partager

    <?php
    
    namespace Entity;
    
    use Doctrine\Common\Collections\ArrayCollection;
    
    class ManyToManyShared {
        /**
         * @ManyToMany(targetEntity="Entity\\Users")
         */
        private $members;
    
        public function __construct()
        {
            $this->owners = new ArrayCollection();
            $this->members = new ArrayCollection();
        }
    
        public function isContainMember()
        {
    
        }
        
        public function getMemberCollection()
        {
            
        }
    }