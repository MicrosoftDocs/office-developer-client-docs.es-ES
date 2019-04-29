---
title: Acerca de las direcciones URL MAPI para la indización basada en notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: 5a3e45809f36b71968560a4b239e268addf00474
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422484"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Acerca de las direcciones URL MAPI para la indización basada en notificaciones

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un proveedor de almacenamiento notifica a un indizador que un objeto está preparado para la indización, genera una dirección URL MAPI que identifica de forma exclusiva el objeto en el controlador de protocolo MAPI. Las direcciones URL de MAPI se codifican en Unicode y tienen el siguiente formato: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

En la tabla siguiente se describen las distintas partes de una dirección URL típica.

|Part | Descripción|
|:----|:-----------|  
|*SID* |Identificador de seguridad del usuario actual.| 
|*StoreDisplayName* |Una cadena que especifica el nombre para mostrar del usuario en ese almacén.|
|*HashNumber* |**DWORD** en representación hexadecimal que se calcula en función del identificador de entrada de almacén o la firma de asignación de almacén. Este valor se almacena en el registro y se usará más adelante para identificar el almacén en el controlador de protocolo MAPI.<br/><br/>Este número debe calcularse de forma que minimice las colisiones con otras tiendas. Para el algoritmo que Microsoft Outlook usa para calcular el número de hash, consulte [algoritmo para calcular el número de hash de la tienda](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Número que identifica el tipo de almacén que contiene el objeto que se va a indizar. Los valores posibles son los siguientes:<br/>-0-almacén predeterminado.<br/><br/>-1-almacén delegado, usado para los elementos de delegación almacenados en caché localmente.<br/><br/>-2-carpetas públicas, usadas para favoritos de carpetas públicas.<br/><br/>**Nota**: Si el almacén se está rastreando en lugar de insertado, el valor que se usa es el carácter*X*.| 
|*FolderNameA/.../FolderNameN* |La ruta de acceso desde la raíz del IPM_SUBTREE a la carpeta o el mensaje. Por ejemplo, un mensaje de la carpeta de **familia** en la **bandeja de entrada** tiene la **bandeja de entrada o familia** para este parámetro. |
|*EntryIDEncoded* |IDENTIFICADOR de entrada MAPI para el elemento codificado como una cadena Unicode. Consulte la siguiente sección "caracteres especiales" para obtener información sobre cómo se codifican determinados caracteres especiales. Para obtener más información acerca del algoritmo para codificar el identificador de entrada, consulte [algoritmo para codificar identificadores de entrada y de datos](algorithm-to-encode-entry-ids-and-attachment-ids.md)adjuntos.<br/><br/>**Nota**: cuando se muestra como texto, este identificador de entrada codificado aparece como cuadros o caracteres hangul aleatorios en cumplimiento con el algoritmo, en función de las fuentes disponibles.  |
|*AttachIDEncoded* |IDENTIFICADOR de datos adJuntos codificado como una cadena Unicode. Consulte la siguiente sección "caracteres especiales" para obtener información sobre cómo se codifican determinados caracteres especiales. Para obtener más información acerca del algoritmo para codificar el identificador de entrada, consulte [algoritmo para codificar identificadores de entrada y de datos](algorithm-to-encode-entry-ids-and-attachment-ids.md)adjuntos.<br/><br/>**Nota**: cuando se muestra como texto, este identificador de entrada codificado aparece como cuadros o caracteres hangul aleatorios en cumplimiento con el algoritmo, en función de las fuentes disponibles. |
|*FileName* |Nombre del archivo de datos adjuntos, tal y como aparece en el mensaje.|
    
## <a name="examples-of-mapi-urls"></a>Ejemplos de direcciones URL de MAPI

A continuación se muestran algunos ejemplos de direcciones URL de MAPI.
  
- Dirección URL MAPI para una carpeta: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- Dirección URL MAPI de un mensaje: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- Dirección URL MAPI para datos adjuntos: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caracteres especiales

Determinados caracteres se codifican si aparecen en el mensaje o los datos adjuntos. A continuación, se muestran los caracteres codificados en una dirección URL MAPI:
  
- % >% 25
    
- />% 2F 
    
- \ >% 5C 
    
- \*>% 2A 
    
- ? >% 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>BLOB asociado a cada dirección URL MAPI

Cuando se inserta una dirección URL MAPI para un objeto que se va a indizar, un proveedor de almacén también crea un objeto binario grande (BLOB) que contiene determinada información para el controlador de protocolo MAPI. El proveedor del almacén asocia este BLOB con cada dirección URL MAPI y lo envía al insertar la dirección URL MAPI en el indizador. El formato del BLOB es el siguiente: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

El proveedor de almacén debe escribir estos valores en el BLOB en el orden que se muestra. En la tabla siguiente se describe cada uno de los campos del BLOB.

|Part | Descripción|
|:----|:-----------|  
|*dwVersion* |Esta es la versión de los datos que se están enviando. Actualmente, este valor es 1.|
|*dwFlags* |Reservado para uso futuro. Actualmente, este valor debe ser 0.|
|*cbProfileName* |El tamaño del nombre del perfil, en bytes. Esta información es útil para que el controlador del protocolo MAPI sepa qué perfil usar al indizar el elemento.|
|*wszProfileName* |Cadena Unicode terminada en null que contiene el nombre del perfil.|
|*cbProviderItemID* |Tamaño del identificador de elemento del proveedor, en bytes. El proveedor de almacenamiento debe enviar solo el identificador de elemento de proveedor para las carpetas, para evitar que se abran carpetas adicionales para obtener esta información.|
|*wszProviderItemID* |Cadena Unicode terminada en NULL con el identificador de elemento de proveedor que identifica de forma única el elemento en el almacén.|
    
## <a name="see-also"></a>Ver también

- [Acerca de la indización de almacén basada en notificaciones](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

