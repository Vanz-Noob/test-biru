# Gunakan image node.js sebagai base image
FROM node:16

# Setel direktori kerja di dalam container
WORKDIR /app

# Copy package.json dan package-lock.json
COPY package.json package-lock.json ./

# Install dependencies
RUN npm install

# Copy seluruh aplikasi ke dalam container
COPY . .

# Build aplikasi React
RUN npm run build

# Setel port yang akan digunakan oleh aplikasi
EXPOSE 3000

# Jalankan aplikasi menggunakan serve
CMD ["npx", "serve", "build"]
