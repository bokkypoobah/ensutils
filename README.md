# ensutils
ENS Utilities


```
{id: "[account]", expiryDate: 1693980763}

query getNames($id: ID!, $expiryDate: Int) {
  account(id: $id) {
    registrations(first: 1000, where: {expiryDate_gt: $expiryDate}) {
      registrationDate
      expiryDate
      domain {
        id
        labelName
        labelhash
        name
        isMigrated
        parent {
          name
          id
        }
        createdAt
      }
    }
    domains(first: 1000) {
      id
      labelName
      labelhash
      name
      isMigrated
      parent {
        name
        id
      }
      createdAt
      registration {
        registrationDate
        expiryDate
      }
    }
    wrappedDomains(first: 1000) {
      expiryDate
      fuses
      domain {
        id
        labelName
        labelhash
        name
        isMigrated
        parent {
          name
          id
        }
        createdAt
        registration {
          registrationDate
          expiryDate
        }
      }
    }
  }
}


```



```

{

  account(id: "[account]") {
    registrations(first: 1000) {
      registrationDate
      expiryDate
      domain {
        id
        labelName
        labelhash
        name
        isMigrated
        parent {
          name
          id
        }
        createdAt
      }
    }
    domains(first: 1000) {
      id
      labelName
      labelhash
      name
      isMigrated
      parent {
        name
        id
      }
      createdAt
      registration {
        registrationDate
        expiryDate
      }
    }
    wrappedDomains(first: 1000) {
      expiryDate
      fuses
      domain {
        id
        labelName
        labelhash
        name
        isMigrated
        parent {
          name
          id
        }
        createdAt
        registration {
          registrationDate
          expiryDate
        }
      }
    }
	}


}
```
