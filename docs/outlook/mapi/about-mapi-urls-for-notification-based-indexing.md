---
title: Acerca de las direcciones URL MAPI Notification-Based indexación
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
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Acerca de las direcciones URL MAPI Notification-Based indexación

**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Cuando un proveedor de almacén notifica a un indizador que un objeto está listo para la indización, genera una dirección URL MAPI que identifica de forma exclusiva el objeto al controlador de protocolo MAPI. Las direcciones URL MAPI se codifican en Unicode y tienen el siguiente formato: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

En la tabla siguiente se describen las distintas partes de una dirección URL típica.

|Parte | Descripción|
|:----|:-----------|  
|*SID* |Identificador de seguridad del usuario actual.| 
|*StoreDisplayName* |Cadena que especifica el nombre para mostrar del usuario en ese almacén.|
|*HashNumber* |**DWORD en** representación hexadecimal que se calcula en función del identificador de entrada del almacén o de la firma de asignación de almacén. Este valor se almacena en el Registro y se usará más adelante para identificar el almacén en el controlador de protocolo MAPI.<br/><br/>Este número debe calcularse de forma que minimice las colisiones con otros almacenes. Para obtener el algoritmo que Microsoft Outlook usa para calcular el número hash, vea [Algoritmo para calcular el número hash del almacén.](algorithm-to-calculate-the-store-hash-number.md)|
|*StoreType* |Número que identifica el tipo de almacén que contiene el objeto que se va a indizar. Los valores posibles son los siguientes:<br/>- 0: almacén predeterminado.<br/><br/>- 1- Almacén delegado, que se usa para los elementos delegados almacenados en caché localmente.<br/><br/>- 2: carpetas públicas, usadas para los favoritos de las carpetas públicas.<br/><br/>**NOTA:** Si el almacén se rastrea en lugar de insertarse, el valor que se usa es el carácter *X*.| 
|*FolderNameA/.../FolderNameN* |Ruta de acceso desde la raíz del IPM_SUBTREE a la carpeta o mensaje. Por ejemplo, un mensaje de la carpeta **Familia** de la **Bandeja de** entrada tiene la Bandeja **de entrada/Familia** para este parámetro. |
|*EntryIDEncoded* |Identificador de entrada MAPI para el elemento codificado como una cadena Unicode. Vea la siguiente sección "Caracteres especiales" para obtener información sobre cómo se codifican determinados caracteres especiales. Para obtener más información acerca del algoritmo para codificar el identificador de entrada, vea Algoritmo para codificar identificadores de entrada e [identificadores de datos adjuntos.](algorithm-to-encode-entry-ids-and-attachment-ids.md)<br/><br/>**NOTA:** Cuando se ve como texto, este identificador de entrada codificada aparece como caracteres hangul aleatorios o cuadros de acuerdo con el algoritmo, en función de las fuentes disponibles.  |
|*AttachIDEncoded* |Identificador de datos adjuntos codificado como una cadena Unicode. Vea la siguiente sección "Caracteres especiales" para obtener información sobre cómo se codifican determinados caracteres especiales. Para obtener más información acerca del algoritmo para codificar el identificador de entrada, vea Algoritmo para codificar identificadores de entrada e [identificadores de datos adjuntos.](algorithm-to-encode-entry-ids-and-attachment-ids.md)<br/><br/>**NOTA:** Cuando se ve como texto, este identificador de entrada codificada aparece como caracteres hangul aleatorios o cuadros de acuerdo con el algoritmo, en función de las fuentes disponibles. |
|*FileName* |Nombre del archivo adjunto, tal como aparece en el mensaje.|
    
## <a name="examples-of-mapi-urls"></a>Ejemplos de direcciones URL MAPI

A continuación se muestran algunos ejemplos de direcciones URL MAPI.
  
- Dirección URL MAPI de una carpeta: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- Dirección URL DE MAPI para un mensaje: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- Dirección URL MAPI para datos adjuntos: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caracteres especiales

Ciertos caracteres se codifican si aparecen en el mensaje o en los datos adjuntos. A continuación se muestran los caracteres que se codifican en una dirección URL MAPI:
  
- % > %25
    
- / > %2F 
    
- \ > %5C 
    
- \* > %2A 
    
- ? > %3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>Blob asociado con cada dirección URL MAPI

Al insertar una dirección URL MAPI para que se indexe un objeto, un proveedor de almacén también crea un objeto binario grande (BLOB) que contiene cierta información para el controlador de protocolo MAPI. El proveedor de almacén asocia este blob con cada dirección URL MAPI y lo envía al insertar la dirección URL MAPI en el indizador. El formato del BLOB es el siguiente: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

El proveedor del almacén debe escribir estos valores en el BLOB en el orden mostrado. En la tabla siguiente se describe cada campo del BLOB.

|Parte | Descripción|
|:----|:-----------|  
|*dwVersion* |Esta es la versión de los datos que se envían. Actualmente, este valor es 1.|
|*dwFlags* |Reservado para uso futuro. Actualmente, este valor debe ser 0.|
|*cbProfileName* |El tamaño del nombre del perfil, en bytes. Esta información es útil para que el controlador de protocolo MAPI sepa qué perfil usar al indizar el elemento.|
|*wszProfileName* |Cadena Unicode terminada en null que contiene el nombre del perfil.|
|*cbProviderItemID* |Tamaño del identificador de elemento del proveedor, en bytes. El proveedor de almacenamiento solo debe enviar el identificador de elemento del proveedor para las carpetas, para evitar abrir carpetas adicionales para obtener esta información.|
|*wszProviderItemID* |Cadena Unicode terminada en null con el identificador de elemento de proveedor que identifica de forma única el elemento en el almacén.|
    
## <a name="see-also"></a>Consulte también

- [Acerca Notification-Based indexación de la Tienda](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

