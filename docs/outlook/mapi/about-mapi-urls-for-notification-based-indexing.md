---
title: Información sobre las direcciones URL de MAPI para la indexación basada en notificaciones
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9cb35f0a-267e-2d85-1701-02d52578a0b8
description: 'Última modificación: 08 de noviembre de 2011'
ms.openlocfilehash: 27ad80b9eca8332beeda147a8b2b4204f9f1cd38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816347"
---
# <a name="about-mapi-urls-for-notification-based-indexing"></a>Información sobre las direcciones URL de MAPI para la indexación basada en notificaciones

**Hace referencia a**: Outlook 
  
Cuando un proveedor de almacén notifica un indizador que un objeto está listo para la indización, genera una dirección URL de MAPI que identifica de forma exclusiva el objeto para el controlador de protocolo MAPI. Direcciones URL de MAPI está codificadas en Unicode y tener el siguiente formato: 
  
`Mapi://SID/StoreDisplayName ($HashNumber)/StoreType/FolderNameA/…/FolderNameN/[EntryIDEncoded[/at=AttachIDEncoded:FileName]]`

En la siguiente tabla se describe las distintas partes de una dirección URL típica.

|Parte | Descripción|
|:----|:-----------|  
|*SID* |Identificador de seguridad del usuario actual.| 
|*StoreDisplayName* |Una cadena que especifica el nombre para mostrar del usuario en dicho almacén.|
|*Hash* |Una **DWORD** en representación hexadecimal que se calcula según el identificador de entrada de almacenamiento o la firma de asignación de almacenamiento. Este valor se almacena en el registro y se usará más adelante para identificar el almacén en el controlador de protocolo MAPI.<br/><br/>Este número se debe calcular en una forma que minimiza los conflictos con otros almacenes. Para el algoritmo que utiliza Microsoft Outlook para calcular el número de hash, vea [algoritmo para calcular el número de Hash de almacén](algorithm-to-calculate-the-store-hash-number.md).|
|*StoreType* |Un número que identifica el tipo del almacén que contiene el objeto que se va a indizar. Los valores posibles son los siguientes:<br/>Almacén de - 0 - predeterminado.<br/><br/>-Almacén delegado 1 -, usado para los elementos de delegado en caché localmente.<br/><br/>-2 - las carpetas públicas, usadas para los favoritos de carpetas públicas.<br/><br/>**Nota**: si el almacén se rastrea en lugar de insertarse, el valor que se utiliza es el carácter*X*.| 
|*FolderNameA/.../FolderNameN* |La ruta de acceso desde la raíz del IPM_SUBTREE a la carpeta o mensaje. Por ejemplo, un mensaje en la carpeta **Bandeja de entrada** **familia** **tiene/Familia de bandeja de entrada** para este parámetro. |
|*EntryIDEncoded* |Identificador de entrada MAPI para el elemento que se codifican como una cadena Unicode. Vea la siguiente sección "Caracteres especiales" para obtener información acerca de cómo se codifican determinados caracteres especiales. Para obtener más información acerca del algoritmo para codificar el identificador de entrada, vea el [algoritmo para codificar identificadores de entrada e identificadores de los datos adjuntos](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Nota**: cuando se ven como texto, esto codificado entrada identificador aparece como aleatorio caracteres Hangul o cuadros de acuerdo con el algoritmo, dependiendo de las fuentes disponibles.  |
|*AttachIDEncoded* |Identificador de datos adjuntos que se codifican como una cadena Unicode. Vea la siguiente sección "Caracteres especiales" para obtener información acerca de cómo se codifican determinados caracteres especiales. Para obtener más información acerca del algoritmo para codificar el identificador de entrada, vea el [algoritmo para codificar identificadores de entrada e identificadores de los datos adjuntos](algorithm-to-encode-entry-ids-and-attachment-ids.md).<br/><br/>**Nota**: cuando se ven como texto, esto codificado entrada identificador aparece como aleatorio caracteres Hangul o cuadros de acuerdo con el algoritmo, dependiendo de las fuentes disponibles. |
|*FileName* |Nombre de los datos adjuntos de archivos, tal como aparece en el mensaje.|
    
## <a name="examples-of-mapi-urls"></a>Ejemplos de direcciones URL MAPI

Los siguientes son algunos ejemplos de direcciones URL de MAPI.
  
- Dirección URL de MAPI para una carpeta: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($be19928f)/2/Office`
    
- Dirección URL de MAPI para un mensaje: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Calendar/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾걤곂갠가`
    
- Dirección URL de MAPI para los datos adjuntos: 
    
  `mapi://S-1-5-21-2127521184-1604012920-1887927527-71418/Mailbox - Some User ($484efb89)/0/Inbox/곯가가가걍걝걌곌겷걢곒갑겛개가검걟곔걙곾간곷갦가/at=겅걋각가:somefile.txt`
    
## <a name="special-characters"></a>Caracteres especiales

Algunos caracteres se codifican si aparecen en el mensaje o datos adjuntos. A continuación muestra qué caracteres se codifican en una dirección URL de MAPI:
  
- % > 25%
    
- / > % 2F 
    
- \ > 5% C 
    
- \*> % 2A 
    
- ? > % 3F 
    
## <a name="blob-associated-with-each-mapi-url"></a>BLOB asociado a cada dirección URL de MAPI

Si se presiona una dirección URL de MAPI para un objeto que se va a indizar, un proveedor de almacén también crea un objeto binario grande (BLOB) que contiene cierta información para el controlador de protocolo MAPI. El proveedor de almacenamiento asocia este BLOB con cada dirección URL de MAPI y lo envía cuando la inserción de la dirección URL de MAPI en el indizador. El formato del objeto binario es como sigue: 
  
```cpp
DWORD  dwVersion
DWORD  dwFlags
ULONG  cbProfileName
WCHAR  wszProfileName
ULONG  cbProviderItemID
WCHAR  wszProviderItemID
```

El proveedor de almacenamiento debe escribir estos valores en el BLOB en el orden mostrado. En la siguiente tabla se describe cada campo del BLOB.

|Parte | Descripción|
|:----|:-----------|  
|*dwVersion* |Esta es la versión de los datos que se está enviados. Actualmente, este valor es 1.|
|*dwFlags* |Reservado para uso posterior. Actualmente, este valor debe ser 0.|
|*cbProfileName* |El tamaño del nombre del perfil, en bytes. Esta información es útil para el controlador de protocolo MAPI saber qué perfil desea utilizar cuando el elemento de la indización.|
|*wszProfileName* |Cadena de Unicode terminada en null que contiene el nombre del perfil.|
|*cbProviderItemID* |Tamaño del identificador de elemento de proveedor, en bytes. El proveedor de almacenamiento debe enviar a sólo el proveedor de identificador de elemento para las carpetas, para impedir la apertura de carpetas adicionales para obtener esta información.|
|*wszProviderItemID* |Cadena de Unicode terminada en null con el identificador de elemento del proveedor que identifica de forma exclusiva el elemento en el almacén.|
    
## <a name="see-also"></a>Vea también

- [Información sobre la indexación de almacenes basada en notificaciones](about-notification-based-store-indexing.md)
- [Constantes MAPI](mapi-constants.md)

