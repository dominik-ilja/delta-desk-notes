<%*
const { constants, ReoccuringTasks } = GIC;
const { DATE_FORMATS } = constants;

const date = moment(tp.file.title, DATE_FORMATS.NOTE.DAY);
const reoccuringTasks = new ReoccuringTasks(date);
const tasks = [
  {
    text: "Bills",
    subTasks: [
      { 
        text: "Waterstone at Big Creek",
        subTasks: [
          { text: "Rent", date: 1 },
          { text: "Community Fee", date: 1 },
          { text: "Utility Fee", date: 1 },
          { text: "Point of Lease Renter's Insurance", date: 1 },
          { text: "Pest Control", date: 1 },
          { text: "Pet Rent", date: 1 },
          { text: "Valet Trash", date: 1 },
        ]
      },
      { text: "Sawnee Electric", date: 1 },
      { text: "Chase Card", date: 3 },
      { text: "Amazon Prime", date: 11 },
      { text: "Phone Plan", date: 13 },
      { text: "Chase Prime Visa", date: 13 },
      { text: "Discover Card", date: 24 },
      { text: "Car Insurance", date: 28 },
      { text: "Discover Card (Kayla)", date: 28 },
    ]
  }
]

tR += reoccuringTasks.create(tasks)
_%>