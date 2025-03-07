project('libbcrypt', 'c')

# List the source files; adjust if libbcrypt has more than one source.
libbcrypt_sources = files('bcrypt.c', 'crypt_blowfish/crypt_blowfish.c', 'crypt_blowfish/crypt_gensalt.c', 'crypt_blowfish/wrapper.c' )

# Build a static library.
libbcrypt_lib = static_library('bcrypt', libbcrypt_sources, install : true)

# Create a dependency object that includes the library and its include directory.
libbcrypt_dep = declare_dependency(
  link_with : libbcrypt_lib,
  include_directories : include_directories('.')
)

# Expose the dependency variable so the parent project can retrieve it.
libbcrypt_dep
