---
title: Secuencia de Autocompletar
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: d4f380fa-2ed9-4c7c-9ef3-b32f8409f657
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: caa93fcc1675531f2d128170c81904e0e286e0f9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: HT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591082"
---
# <a name="autocomplete-stream"></a>Secuencia de Autocompletar

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Además de saber cómo Microsoft Outlook interactúa con la secuencia de autocompletar, también debe comprender el formato binario de la secuencia de autocompletar.
  
La secuencia de autocompletar es un conjunto de filas de la propiedad de destinatario que se guardan como una secuencia binaria con algunos metadatos de contabilidad que solo usan Microsoft Outlook 2013, Microsoft Outlook 2010, Microsoft Office Outlook 2007 y Microsoft Outlook 2003. Los metadatos son relevantes para las interacciones de Outlook con el flujo de autocompletar, por lo que los terceros deben conservar el contenido de cada bloque de metadatos cuando guardan una secuencia de autocompletar modificada. Dicho de otro modo, los terceros deben modificar solo la parte del conjunto de filas del formato binario y conservar el contenido que ya está en los bloques de metadatos de la secuencia de autocompletar.
  
## <a name="stream-visualization"></a>Visualización de flujo

El diseño de alto nivel de la secuencia de autocompletar es el siguiente:
  
Metadatos (4 bytes)
  
Número de versión principal (4 bytes)
  
Número de versión secundaria (4 bytes)
  
Número de filas n (4 bytes)
  
Número de propiedades p de la fila uno (4 bytes)
  
Etiqueta de propiedad de la Propiedad 1 (4 bytes)
  
Datos reservados de la Propiedad 1 (4 bytes)
  
Unión de valor de la Propiedad 1 (8 bytes)
  
Datos del valor de la Propiedad 1 (0 o bytes variables)
  
… (propiedades 2 por P-1)
  
Etiqueta de la propiedad de la Propiedad p (4 bytes)
  
Valor reservado de la Propiedad p (4 bytes)
  
Unión de valor de la Propiedad p (8 bytes)
  
Datos del valor de la Propiedad p (0 o bytes variables)
  
Número de propiedades q de la fila dos (4 bytes)
  
… (propiedades de la fila dos)
  
… (filas 3 a n-1)
  
Número de propiedades p de la fila n (4 bytes)
  
… (propiedades de la fila n)
  
EI de recuento de byte de información adicional (4 bytes)
  
Información adicional (bytes EI)
  
Metadatos (8 bytes)
  
Para obtener un ejemplo de una estructura binaria, vea el ejemplo binario en las [Directrices de desarrollador y formato de archivo NK2 de Outlook 2003/2007.](http://portalvhds6gyn3khqwmgzd.blob.core.windows.net/files/NK2/NK2WithBinaryExample.pdf)
  
## <a name="high-level-layout"></a>Diseño de alto nivel

En términos generales, el diseño de la secuencia de autocompletar es el siguiente:
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Metadatos  <br/> |4  <br/> |
|Número de versión principal  <br/> |4  <br/> |
|Número de versión secundaria  <br/> |4  <br/> |
|Conjunto de filas  <br/> |Variable  <br/> |
|EI de recuento de byte de información adicional  <br/> |4  <br/> |
|Información adicional  <br/> |EI  <br/> |
|Metadatos  <br/> |8  <br/> |
   
Al leer esta secuencia, si la versión principal es diferente de 12, esta secuencia no debe leerse ni escribirse. La versión secundaria actual de la secuencia de autocompletar es 0, que tiene el recuento de byte de información adicional establecido en 0. Si la versión secundaria es distinta de 0, habrá información en la información adicional que debe leerse al leer la secuencia y conservarse cuando se escribe la secuencia. La versión secundaria también deberá conservarse al escribir la secuencia. Si no se conservan ambas, las instancias de Outlook que escribieron la información adicional perderán datos. 
  
> [!NOTE]
> Las aplicaciones no deben agregar datos personalizados en el campo Información adicional o cambiar la versión secundaria, ya que esta funcionalidad admite las extensiones de Outlook en el formato y no extensiones arbitrarias de terceros. 
  
## <a name="row-set-layout"></a>Diseño del conjunto de filas

El diseño del conjunto de filas es el siguiente: 
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de filas  <br/> |4  <br/> |
|Filas  <br/> |Variable  <br/> |
   
El número de filas identifica cuántas filas tiene el siguiente elemento de la secuencia binaria.
  
## <a name="row-layout"></a>Diseño de fila

Cada fila tiene el siguiente formato:
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de propiedades  <br/> |4  <br/> |
|Propiedades  <br/> |Variable  <br/> |
   
El número de propiedades identifica cuántas propiedades tiene el siguiente elemento de la secuencia binaria.
  
## <a name="property-layout"></a>Diseño de propiedad

Cada propiedad tiene el siguiente formato:
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Etiqueta de propiedad  <br/> |4  <br/> |
|Datos reservados  <br/> |4  <br/> |
|Unión de valor de propiedad  <br/> ||
|Información del valor  <br/> |0 o variable (en función de la etiqueta de propiedad)  <br/> |
   
## <a name="interpreting-the-property-value"></a>Interpretar el valor de propiedad

La unión de valor de propiedad y los datos de valor deben interpretarse en función de la etiqueta de propiedad de los 4 primeros bytes del bloque de propiedades. Esta etiqueta de propiedad está en el mismo formato que una etiqueta de propiedad MAPI. Los bits de 0 a 15 de la etiqueta de propiedad son el tipo de propiedad. Los bits de 16 a 31 son el identificador de la propiedad. El tipo de propiedad determina cómo se debe leer el resto de la propiedad.
  
## <a name="static-value"></a>Valor estático

Algunas propiedades no tienen Datos de valor y solo tienen datos en la unión. Los siguientes tipos de propiedades (que proceden de la Etiqueta de propiedad) deben interpretar los datos de la unión de propiedad de 8 bytes como sigue:
  
|**Tipo de propiedad**|**Interpretación de la unión de propiedad**|
|:-----|:-----|
|PT_I2  <br/> |short int  <br/> |
|PT_LONG  <br/> |long  <br/> |
|PT_R4  <br/> |float  <br/> |
|PT_DOUBLE  <br/> |double  <br/> |
|PT_BOOLEAN  <br/> |short int  <br/> |
|PT_SYSTIME  <br/> |FILETIME  <br/> |
|PT_I8  <br/> |LARGE_INTEGER  <br/> |
   
## <a name="dynamic-values"></a>Valores dinámicos

Otras propiedades tienen datos en un bloque de Datos del valor después de los primeros 16 bytes que contienen la Etiqueta de propiedad, los Datos reservados y la Unión de valor de propiedad. A diferencia de los valores estáticos, los datos almacenados en la Unión de valor de propiedad de 8 bytes son irrelevantes al leer. Al escribir, asegúrese de rellenar estos 8 bytes con algo. Sin embargo, no es importante el contenido de los 8 bytes. En los valores dinámicos, el tipo de etiqueta de propiedad determina cómo interpretar los Datos de valor.
  
PT_STRING8 
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4  <br/> |
|Bytes que se interpretarán como una cadena de ANSI (incluye terminador NULL)  <br/> |n  <br/> |
   
PT_CLSID
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Bytes que se interpretarán como un GUID  <br/> |16  <br/> |
|||
   
PT_BINARY 
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4  <br/> |
|Bytes que se interpretarán como una matriz de bytes  <br/> |n  <br/> |
   
PT_ERROR
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de bytes n  <br/> |4  <br/> |
|Bytes que se interpretarán como una matriz de bytes  <br/> |n  <br/> |
   
PT_MV_BINARY
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de matrices binarias X  <br/> |4  <br/> |
|Una ejecución de bytes que contiene X matrices binarias. Cada matriz debe interpretarse exactamente igual al byte PT_BINARY ejecutado.  <br/> |Variable  <br/> |
   
PT_MV_STRING8 (Outlook 2007, Outlook 2010 y Outlook 2013)
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de cadenas ANSI X  <br/> |4  <br/> |
|Una ejecución de bytes que contiene las cadenas ANSI X. Cada cadena debe interpretarse exactamente igual al byte PT_STRING8 ejecutado.  <br/> |Variable  <br/> |
   
PT_MV_UNICODE (Outlook 2007, Outlook 2010, Outlook 2013)
  
|**Datos de valor**|**Número de bytes**|
|:-----|:-----|
|Número de cadenas UNICODE X  <br/> |4  <br/> |
|Una ejecución de bytes que contiene X cadenas UNICODE. Cada cadena debe interpretarse exactamente igual al byte PT_UNICODE ejecutado.  <br/> |Variable  <br/> |
   
## <a name="significant-properties"></a>Propiedades importantes

Como se indicó anteriormente en este tema, los bloques binarios que representan las propiedades tienen etiquetas de propiedades que se corresponden a propiedades de los destinatarios de la libreta de direcciones. Para propiedades que no se muestran aquí, puede buscar la descripción de la propiedad en http://msdn.microsoft.com/en-us/library/cc433490(EXCHG.80).aspx.
  
|**Nombre de propiedad**|**Etiqueta de propiedad**|**Descripción (vea MSDN para obtener más información)**|
|:-----|:-----|:-----|
|PR_NICK_NAME_W (no se transmite en destinatarios, específica solo para la secuencia de autocompletar)  <br/> |0x6001001f  <br/> |Esta propiedad debe ser la primera en cada fila del destinatario. Actúa como un identificador de clave de la fila del destinatario.  <br/> |
|PR_ENTRYID  <br/> |0x0FFF0102  <br/> |El identificador de entrada de la libreta de direcciones del destinatario.  <br/> |
|PR_DISPLAY_NAME_W  <br/> |0x3001001F  <br/> |El nombre para mostrar del destinatario.  <br/> |
|PR_EMAIL_ADDRESS_W  <br/> |0x3003001F  <br/> |La dirección de correo electrónico del destinatario (por ejemplo, juanperez@contoso.com o /o=Contoso/OU=Foo/cn=Recipients/cn=juanperez)  <br/> |
|PR_ADDRTYPE_W  <br/> |0x3002001F  <br/> |Tipo de dirección del destinatario (por ejemplo, SMTP o EX).  <br/> |
|PR_SEARCH_KEY  <br/> |0x300B0102  <br/> |La clave de búsqueda MAPI del destinatario.  <br/> |
|PR_SMTP_ADDRESS_W  <br/> |0x39FE001f  <br/> |La dirección de SMTP del destinatario.  <br/> |
|PR_DROPDOWN_DISPLAY_NAME_W (no se transmite en destinatarios, específica solo para la secuencia de autocompletar)  <br/> |0X6003001f  <br/> |La cadena para mostrar que aparece en la lista Autocompletar.  <br/> |
|PR_NICK_NAME_WEIGHT (no se transmite en destinatarios, específica solo para la secuencia de autocompletar)  <br/> |0x60040003  <br/> |El peso de esta entrada de autocompletar. El peso se usa para determinar en qué orden se producen las entradas de autocompletar cuando coinciden con la lista autocompletar. Se mostrarán las entradas con mayor peso antes que las entradas con un peso inferior. Esta propiedad ordena la lista completa de autocompletar. El peso disminuye periódicamente con el tiempo y aumenta cuando el usuario envía un correo electrónico a este destinatario. Vea la descripción más adelante en este tema para obtener más información sobre esta propiedad.  <br/> |
   
PR_NICK_NAME_WEIGHT
  
La propiedad PR_NICK_NAME_WEIGHT ordena el conjunto de filas de la secuencia de autocompletar en orden descendente y la secuencia de autocompletar siempre debe conservar esta característica ordenada. Por lo tanto, los cambios realizados en el peso de una fila también deben asegurar que la posición de la fila mantiene el criterio de ordenación de un conjunto completo de filas. Cualquier adición al conjunto de filas debe insertarse en la posición para mantener el orden correcto.
  
El valor mínimo de este peso es 0x1 y el valor máximo es LONG_MAX. Otros valores para el peso se consideran no válidos.
  
Cuando Outlook 2007 envía un correo o resuelve a un destinatario, aumentará el peso del destinatario en 0x2000.
  

