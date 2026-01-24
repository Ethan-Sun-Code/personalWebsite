<script setup>
import { BookOpen, Award } from 'lucide-vue-next'

const journals = [
  {
    title: '3D tensile fracture analysis of tailored fibre placement composites using digital volume correlation',
    authors: 'Sun, G., Mitchell, R.L., Chen, Z., Omrani, F., Smith, M., Frias, C., Fairclough, J.P.A. and Pinna, C.',
    journal: 'Theoretical and Applied Fracture Mechanics',
    year: '2025',
    details: 'p.105127',
    doi: 'https://doi.org/10.1016/j.tafmec.2025.105127'
  },
  {
    title: 'X-ray Computed Tomography Characterisation of Damage Development during in-situ Tensile Testing of Carbon Fibre Composites Manufactured through Tailored Fibre Placement',
    authors: 'Sun, G., Mitchell, R.L., Chen, Z., Omrani, F., Smith, M., Frias, C., Fairclough, J.P.A. and Pinna, C.',
    journal: 'Submitted to Composite Part A',
    year: 'Under Review',
    details: ''
  },
  {
    title: 'Short-term moisture effects on the flexural performance of sustainable flax-epoxy and carbon-flax-carbon (CFC) composites',
    authors: 'G. Sun, T. Murmu, A. A. Abdel-Wahab, T. Leslie, B. Rakshani, O. Obeid',
    journal: 'Submitted to Journal of Natural Fibres',
    year: 'Under Revision',
    details: ''
  }
]

const conferences = [
  {
    title: '3D characterisation of local deformation and damage development in tailored fibre placement-manufactured composites under tensile loading',
    authors: 'Sun, G., Mitchell, R., Chen, Z., Smith, M., Omrani, F., Fairclough, P. and Pinna, C.',
    conference: 'SAMPE Europe 24',
    location: '',
    year: '2024',
    details: 'Vol. 2, pp. 1050-1058'
  },
  {
    title: '3D characterisation of the tensile failure of CFRPS manufactured through tailored fibre placement',
    authors: 'Sun, G., Mitchell, R., Chen, Z., Omrani, F., Smith, M., Fairclough, J.P.A. and Pinna, C.',
    conference: '2023 International Conference on Composite Materials (ICCM23)',
    location: 'Belfast, Northern Ireland',
    year: '2023',
    details: 'July 2023'
  }
]
</script>

<template>
  <section id="publications" class="section">
    <div class="container">
      <h2 class="section-title">发表论文 & 会议</h2>
      
      <div class="publication-category">
        <h3 class="category-title"><BookOpen size="24" /> 期刊论文 (Journal Publications)</h3>
        <div class="publication-list">
          <div v-for="(paper, index) in journals" :key="index" class="publication-item card">
            <h4 class="paper-title">{{ paper.title }}</h4>
            <p class="authors">{{ paper.authors }}</p>
            <div class="meta">
              <span class="journal-name">{{ paper.journal }}</span>
              <span v-if="paper.year" class="year">{{ paper.year }}</span>
              <span v-if="paper.details" class="details">{{ paper.details }}</span>
            </div>
            <a v-if="paper.doi" :href="paper.doi" target="_blank" class="doi-link">View DOI</a>
          </div>
        </div>
      </div>

      <div class="publication-category">
        <h3 class="category-title"><Award size="24" /> 会议论文 (Conference Papers)</h3>
        <div class="publication-list">
          <div v-for="(paper, index) in conferences" :key="index" class="publication-item card">
            <h4 class="paper-title">{{ paper.title }}</h4>
            <p class="authors">{{ paper.authors }}</p>
            <div class="meta">
              <span class="conference-name">{{ paper.conference }}</span>
              <span v-if="paper.location" class="location">{{ paper.location }}</span>
              <span class="year">{{ paper.year }}</span>
            </div>
            <p v-if="paper.details" class="details">{{ paper.details }}</p>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
.publication-category {
  margin-bottom: 3rem;
}

.category-title {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  font-size: 1.5rem;
  color: var(--primary-color);
  margin-bottom: 1.5rem;
  border-bottom: 2px solid var(--border-color);
  padding-bottom: 0.5rem;
}

.publication-list {
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
}

.publication-item {
  border-left: 4px solid var(--accent-color);
}

.paper-title {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: var(--text-primary);
}

.authors {
  font-size: 0.95rem;
  color: var(--text-secondary);
  margin-bottom: 0.5rem;
  font-style: italic;
}

.meta {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  font-size: 0.9rem;
  color: var(--text-primary);
  align-items: center;
}

.journal-name, .conference-name {
  font-weight: 600;
  color: var(--primary-color);
}

.doi-link {
  display: inline-block;
  margin-top: 0.75rem;
  font-size: 0.85rem;
  color: var(--accent-color);
  text-decoration: none;
  font-weight: 500;
}

.doi-link:hover {
  text-decoration: underline;
}
</style>