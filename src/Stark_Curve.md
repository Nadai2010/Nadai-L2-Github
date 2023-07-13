Starknet AA

Esperamos que haya disfrutado de la primera parte, donde se presentaron conceptos generales de criptografía. Ahora nos adentraremos en un tema aún más interesante, Starknet y cómo mejora el ecosistema, exploraremos cómo los contratos de cuentas (CA) y el esquema de firmas abstraídas de Starknet ofrecen beneficios significativos frente al  ERC-4337.

Si deseas aprender más sobre el concepto y las variantes del ERC-4337, te recomendamos leer esta serie de artículos en el blog de Argent. La serie está compuesta por la Parte 1, Parte 2 y Parte 3 . Argent y Braavos son Smart wallets que aprovechan el poder del AA nativo en Starknet. También te recomendamos leer los artículos de Braavos de Guide 101 AA y Security Pyramid AA, los cuales presentan optimizaciones adicionales y capas de seguridad que exploraremos más adelante. Estos recursos te proporcionarán una mejor comprensión del concepto de AA y del ERC-4337.

¡Así que sin más preámbulos, bienvenidos a Starknet!

En el ecosistema de Starknet, se encuentran diversas metodologías para generar claves y firmas. A diferencia de las cuentas EOA, en Starknet se emplea Account Abstraction (AA) para la implementación de Contratct Accounts (CA). Estos contratos son responsables de establecer la lógica en nuestras cuentas dentro de Starknet, incluyendo la validación del esquema de firma abstraído.

En lugar de utilizar ECDSA, Starknet utiliza una variación llamada STARK Curve, un tipo de curva elíptica más amigable y optimizada que es nativa en en el ecosistema, esta variante nos ofrece mejoras y características específicas para las necesidades de Starknet.

Lo grandioso de tener esta abstracción nativa es que permite añadir diferentes lógicas en tus esquemas o capas adicionales. Normalmente, se utiliza el sistema asimétrico secp256k1, basado en la aleatoriedad y operaciones matemáticas, para generar claves privadas y públicas. Sin embargo, también se pueden añadir curvas adicionales de forma nativa al crear un CA, como lo ha hecho Braavos con la secp256r1. Esta curva cuenta con un sistema de firmas integrado, mejor optimizado y preparado para dispositivos modernos, donde el signer puede almacenar los datos habilitados por biometricidad en dispositivos aislados y seguros, como el módulo "Enclave" de Apple.

La AA desempeña un papel crucial al abstraer el esquema de firmas o verificación de firmas de la ejecución. Como vimos anteriormente, ECDSA genera una clave privada y una clave pública que luego se cifran y se comparten públicamente, en este caso el poseedor de esta clave privada y del esquema de firma asociado tiene el poder de realizar transacciones en Starknet, los dos tipos de transacciones son DEPLOY o INVOKE