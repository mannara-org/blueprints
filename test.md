```dbml

// 1. Pedagogical Structure

// We mean by 'Pedagogical' the hierarchy of groupings that students are
// divided in.
//
// The structure is pretty straightforward. A specialty has academic levels
// that each contain sections which are in turn also divided in groups.
//
// Each group must have a teaching assistant.


Table students {
  id integer [pk, increment]
  group_id integer [not null]
  surname text [not null]
  name text
  matricule text
  email text
}


Table groups {
  id integer [pk, increment]
  number integer [not null]
  teaching_assistant_id integer [not null]
  section_id integer [not null]
}


Table teaching_assistants {
  id integer [pk, increment]
  surname text [not null]
  name text [not null]
  email text [not null]
  phone_number text
}


Table sections {
  id integer [pk, increment]
  academic_level_id integer [not null]
  identifier text [not null]
}


Table academic_levels {
  id integer [pk, increment]
  level integer [not null]
  specialty_id integer [not null]
}


Table specialties {
  id integer [pk, increment]
  // e.g. "Intelligence Artificiel" or "Science et Technologies"
  name text [not null]
  // an abreviation of the name e.g. "AI" or "GL" for "Genie Logiciel"
  acronyme text [not null]
  // wether it's a Master's specialty or a Licence one
  cycle text [not null]
}


Ref: students.group_id > groups.id

Ref: groups.section_id > sections.id

Ref: groups.teaching_assistant_id > teaching_assistants.id

Ref: sections.academic_level_id > academic_levels.id

Ref: academic_levels.specialty_id > specialties.id

// @pos students 726 588
// @pos groups 73 155
// @pos teaching_assistants 553 19
// @pos sections 549 238
// @view -112 25 0.647
```

# He

