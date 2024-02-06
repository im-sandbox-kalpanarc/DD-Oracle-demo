**Issue Template**

### Description
[Describe the issue or feature request here]

### Steps to Reproduce
[Provide steps to reproduce the issue, if applicable]

### Expected Behavior
[Describe what you expected to happen]

### Actual Behavior
[Describe what actually happened]

### Branch (please select the appropriate branch)
<details>
<summary>Click to select branch</summary>

<select id="branchSelect">
  <!-- JavaScript will populate options here -->
</select>

<script>
  // Fetch branches dynamically using GitHub API
  fetch("https://api.github.com/repos/<owner>/<repo>/branches")
    .then(response => response.json())
    .then(data => {
      const branchSelect = document.getElementById("branchSelect");
      data.forEach(branch => {
        const option = document.createElement("option");
        option.text = branch.name;
        option.value = branch.name;
        branchSelect.appendChild(option);
      });
    })
    .catch(error => {
      console.error("Error fetching branches:", error);
    });
</script>
</details>
