<script setup>
const validateDelimiter = (input) => {
  const inputWithoutSpaces = input.replace(/\s/g, '').split(',');
  return inputWithoutSpaces.filter((item) => item.length >= 2);
}

const resolver = (inp) => {
  let matches = [];

  let formatted = inp.substring(0, 2).toUpperCase();
  let formatted3 = inp.substring(0, 3).toUpperCase();
  
  if ([
    "ΥΑ", "ΥΒ", "ΥΕ", "ΥΖ", "ΥΗ", "ΖΖ", "ΖΗ", "ΖΚ", "ΖΜ", "ΙΒ", "ΙΕ", "ΙΖ", "ΙΗ", "ΙΚ", "ΙΜ", "ΙΟ", "ΙΡ", "ΙΤ", "ΙΥ", "ΧΕ", "ΧΖ", "ΧΗ", "ΧΡ", "ΧΤ", "ΧΥ", "ΧΧ", "ΗΒ", "ΟΑ", "ΟΒ", "ΟΕ", "ΟΖ", "ΟΗ", "ΟI", "ΟΚ", "ΟΜ", "ΟΝ", "ΟΟ", "ΟΤ", "ΟΥ", "ΟΧ", "ΧΜ", "ΖΕ", "ΖΙ", "ΖΟ"
  ].includes(formatted)) {
    matches.push("Αθήνα");
  }

    if ([
        "ΥΙ", "ΥΚ", "ΥΜ", "ΥΝ", "ΖΝ", "ΖΡ", "ΒΕ", "ΒΖ", "ΒΗ", "ΒΧ", "ΤΖ"
    ].includes(formatted)) {
        matches.push("Πειραιά");
    }

    if ([
        "ΥΟ", "ΥΡ", "ΥΤ", "ΖΤ", "ΒΝ", "ΒΡ"
    ].includes(formatted)) {
        matches.push("Δυτική Αττική (Ελευσίνα)");
    }

    if ([
        "ΥΧ", "ΥΥ", "ΖΧ", "ΖΥ", "ΒΚ", "ΒΜ"
    ].includes(formatted)) {
        matches.push("Ανατολική Αττική (Παλλήνη)");
    }

    if ([
        "ΜΕ"
    ].includes(formatted)) {
        matches.push("Αιτωλοακαρνανία (Μεσολόγγι)");
    }

    if ([
        "ΑΙ", "ΤΗ"
    ].includes(formatted)) {
        matches.push("Αιτωλοακαρνανία (Αγρίνιο)");
    }

    if ([
        "ΑΡ", "ΤΜ"
    ].includes(formatted)) {
        matches.push("Αργολίδα (Ναύπλιο)");
    }

    if ([
        "ΤΡ"
    ].includes(formatted)) {
        matches.push("Αρκαδία (Τρίπολη)");
    }

    if ([
        "ΑΤ"
    ].includes(formatted)) {
        matches.push("Άρτα");
    }

    if ([
        "ΑΧ", "ΑΖ", "ΑΟ", "ΑΑ", "ΑΥ"
    ].includes(formatted)) {
        matches.push("Αχαΐα (Πάτρα)");
    }

    if ([
        "ΒΙ", "ΒΥ"
    ].includes(formatted)) {
        matches.push("Βοιωτία (Λιβαδειά)");
    }

    if ([
        "ΡΝ"
    ].includes(formatted)) {
        matches.push("Γρεβενά");
    }

    if ([
        "ΡΜ", "ΤΟ"
    ].includes(formatted)) {
        matches.push("Δράμα");
    }


    if ([
        "ΡΟ", "ΡΚ", "ΡΥ", "ΡΧ"
    ].includes(formatted)) {
        matches.push("Δωδεκάνησα (Ρόδος)");
    }

    if([
        "ΚΧ", "ΕΑ"
    ].includes(formatted)) {
        matches.push("Δωδεκάνησα (Κως)");
    }

    if ([
        "ΕΒ", "ΜΧ"
    ].includes(formatted)) {
        matches.push("Έβρος (Αλεξανδρούπολη)");
    }

    if ([
        "ΟΡ"
    ].includes(formatted)) {
        matches.push("Έβρος (Ορεστιάδα)");
    }

    if ([
        "ΧΑ", "ΕΗ", "ΕΙ"
    ].includes(formatted)) {
        matches.push("Εύβοια (Χαλκίδα)");
    }

    if ([
        "ΚΗ"
    ].includes(formatted)) {
        matches.push("Ευρυτανία (Καρπενήσι)");
    }

    if ([
        "ΖΑ", "ΖΒ"
    ].includes(formatted)) {
        matches.push("Ζάκυνθος");
    }

    if ([
        "ΗΑ", "ΗΕ"
    ].includes(formatted)) {
        matches.push("Ηλεία (Πύργος)");
    }

    if ([
        "ΗΜ", "ΗΧ"
    ].includes(formatted)) {
        matches.push("Ημαθία (Βέροια)");
    }

    if ([
        "ΗΡ", "ΗΚ", "ΗΖ", "ΗΗ", "ΗΙ", "ΗΤ"
    ].includes(formatted)) {
        matches.push("Ηράκλειο");
    }

    if ([
        "ΗΝ"
    ].includes(formatted)) {
        matches.push("Θεσπρωτία (Ηγουμενίτσα)");
    }

    if ([
        "ΝΑ", "ΝΒ", "ΝΕ", "ΝΖ", "ΝΗ", "ΝΙ", "ΝΚ", "ΝΜ", "ΝΝ", "ΝΟ", "ΝΡ", "ΝΤ", "ΝΥ", "ΝΧ"
    ].includes(formatted)) {
        matches.push("Θεσσαλονίκη");
    }

    if ([
        "ΙΝ", "ΙΙ"
    ].includes(formatted)) {
        matches.push("Ιωάννινα");
    }

    if ([
        "ΚΒ", "ΑΒ"
    ].includes(formatted)) {
        matches.push("Καβάλα");
    }

    if ([
      "ΚΑ", "ΜΚ"
    ].includes(formatted)) {
      matches.push("Ηράκλειο");
    }

    if ([
      "ΚΤ"
    ].includes(formatted)) {
      matches.push("Καστοριά");
    }

    if ([
      "ΚΥ", "ΕΤ", "ΤΒ", "ΤΕ"
    ].includes(formatted)) {
      matches.push("Κέρκυρα");
    }

    if ([
      "ΚΕ"
    ].includes(formatted)) {
      matches.push("Κεφαλληνία");
    }

    if ([
      "ΚΙ", "ΕΧ"
    ].includes(formatted)) {
      matches.push("Κιλκίς");
    }

    if ([
      "ΚΖ", "ΜΝ"
    ].includes(formatted)) {
      matches.push("Κοζάνη");
    }

    if ([
      "ΚΡ", "ΡΒ"
    ].includes(formatted)) {
      matches.push("Κορινθία");
    }

    if ([
      "ΕΜ", "ΕΖ", "ΕΝ", "ΕΟ"
    ].includes(formatted)) {
      matches.push("Κυκλάδες (Ερμούπολη)");
    }

    if ([
      "ΑΚ", "ΜΡ"
    ].includes(formatted)) {
      matches.push("Λακωνία");
    }

    if ([
      "ΡΙ", "ΡΡ", "ΡΤ"
    ].includes(formatted)) {
      matches.push("Λάρισα");
    }

    if ([
      "ΑΝ", "ΑΕ"
    ].includes(formatted)) {
      matches.push("Λασίθι (Αγ. Νικόλαος)");
    }

    if ([
      "ΜΥ", "ΜΤ"
    ].includes(formatted)) {
      matches.push("Λέσβος (Μυτιλήνη)");
    }

    if ([
      "ΜΗ"
    ].includes(formatted)) {
      matches.push("Λέσβος (Μυρίνα Λήμνου)");
    }

    if ([
      "ΕΥ"
    ].includes(formatted)) {
      matches.push("Λευκάδα");
    }

    if ([
      "ΒΟ", "ΒΒ", "ΒΑ", "ΒΤ"
    ].includes(formatted)) {
      matches.push("Μαγνησία (Βόλος)");
    }

    if ([
      "ΚΜ", "ΜΖ"
    ].includes(formatted)) {
      matches.push("Μεσσηνία (Καλαμάτα)");
    }

    if ([
      "ΑΗ", "ΗΟ"
    ].includes(formatted)) {
      matches.push("Ξάνθη");
    }

    if ([
      "ΕΕ", "ΜΜ"
    ].includes(formatted)) {
      matches.push("Πέλλα (Έδεσσα)");
    }

    if ([
      "ΚΝ", "ΤΙ"
    ].includes(formatted)) {
      matches.push("Πιερία (Κατερίνη)");
    }

    if ([
      "ΡΖ", "ΤΧ"
    ].includes(formatted)) {
      matches.push("Πρέβεζα");
    }

    if ([
      "ΡΕ", "ΡΗ"
    ].includes(formatted)) {
      matches.push("Ρέθυμνο");
    }

    if ([
      "ΚΚ", "ΤΤ", "ΚΟ"
    ].includes(formatted)) {
      matches.push("Ροδόπη (Κομοτηνή)");
    }

    if ([
      "ΜΟ", "ΜΒ"
    ].includes(formatted)) {
      matches.push("Σάμος");
    }

    if ([
      "ΕΡ", "ΙΧ"
    ].includes(formatted)) {
      matches.push("Σέρρες");
    }

    if ([
      "ΤΝ", "ΤΚ"
    ].includes(formatted)) {
      matches.push("Τρίκαλα");
    }
  
    if ([
      "ΜΙ", "ΗΥ"
    ].includes(formatted)) {
      matches.push("Φθιώτιδα (Λαμία)");
    }

    if ([
      "ΡΑ"
    ].includes(formatted)) {
      matches.push("Φλώρινα");
    }

    if ([
      "ΑΜ"
    ].includes(formatted)) {
      matches.push("Φωκίδα (Άμφισσα)");
    }

    if ([
      "ΧΚ", "ΜΑ"
    ].includes(formatted)) {
      matches.push("Χαλκιδική (Πολύγυρος)");
    }

    if ([
      "ΧΝ", "ΧΒ", "ΤΥ"
    ].includes(formatted)) {
      matches.push("Χανιά");
    }

    if ([
      "ΧΙ", "ΧΟ"
    ].includes(formatted)) {
      matches.push("Χίος");
    }

    if ([
      "ΚΟΚ"
    ].includes(formatted3)) {
      matches.push("Θεσσαλονίκη (Κατ' εξαίρεση)");
    }

    if (matches.length === 0) {
      matches.push("unknown");
    }

  return matches.join(", ");
}

const str = ref();
const results = useState("results", () => []);

onMounted(() => {
  watch(str, (newVal) => {
    results.value = [];
    console.log(newVal, validateDelimiter(newVal))
    validateDelimiter(newVal).forEach((item) => {
      results.value.push({
        pref: item,
        matches: resolver(item)
      })
    });
  });
})
</script>

<template>
    <StructuresFlex column class="p-2 gap-3 pt-6 items-center">
      <h1 class="text-xl">Εισάγετε πρόθεματα πινακίδας διαχωρισμένα με κόμμα για αναζήτηση</h1>
      <StructuresFlex column class="gap-6">
        <UInput v-model="str" icon="i-heroicons-magnifying-glass-20-solid" color="white" size="lg" :trailing="false" placeholder="(π.χ ΥΤΟ, ΧΚΑ, κτλ)" />
        <Result v-for="res in results" :pref="res" />
      </StructuresFlex>
    </StructuresFlex>
</template>
