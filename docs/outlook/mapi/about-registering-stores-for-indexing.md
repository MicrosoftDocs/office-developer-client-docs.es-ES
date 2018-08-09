---
title: Información sobre el registro de almacenes de indexación
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: dd2aa06a-96e8-1291-18b5-fc3c40b74e4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b16446644c360185908e7f4e58463257fe17f403
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816372"
---
# <a name="about-registering-stores-for-indexing"></a>Información sobre el registro de almacenes de indexación

  
  
**Hace referencia a**: Outlook 
  
En este tema es específico para la búsqueda instantánea de Microsoft Office Outlook 2007.
  
Búsqueda instantánea le permite encontrar rápidamente los elementos de Outlook. Utiliza los componentes de Windows Desktop Search.
  
El controlador de protocolo MAPI comprueba el registro de Windows para los almacenes que deben indizar para fines de búsqueda. Los proveedores de almacén que desean indizar deben estar registrados en el registro de Windows.
  
De forma predeterminada, Windows Desktop Search agrega los siguientes cuatro tipos de los proveedores de almacén para el registro de Windows para permitir la indización:
  
- Almacén de archivos de carpetas personales (. PST).
    
-  Almacén de Microsoft Exchange, incluidos los archivos de carpetas sin conexión (.ost). 
    
-  Almacén de carpetas públicas. 
    
-  Almacén para Microsoft Office Outlook Connector para MSN. 
    
 Los proveedores de almacén de otro fabricante que desean que se indice deben registrarse en el registro de Windows. 
  
> [!NOTE]
> Los administradores y usuarios pueden usar una configuración de directiva de grupo para impedir la indización de los elementos de Outlook de Windows Desktop Search. Para obtener más información, vea [Ampliación de Windows Desktop Search](http://msdn.microsoft.com/library/2eab146a-8516-4b95-b73c-ca7f980ba233%28Office.15%29.aspx). 
  
## <a name="registry-keys"></a>Claves del registro

En un equipo, todos los proveedores de almacén que desean indizar deben estar registrados en sólo uno de los siguientes tres claves del registro en el registro de Windows. El controlador de protocolo MAPI tiene el aspecto bajo cada una de estas claves en el orden siguiente:
  
1. \Software\Policies\Microsoft\Windows\Windows Search\ [HKLM]
    
2. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKLM]
    
3. \Software\Microsoft\Windows\Windows Search\Preferences\ [HKCU]
    
 Cada valor en la clave corresponde a un proveedor de almacén que se van a indizar. El nombre del valor es el identificador único global (GUID) del proveedor de almacenamiento, que es del tipo **DWORD** y tiene el valor hexadecimal 0 x 00000001. 
  
## <a name="guids-for-store-providers"></a>GUID de los proveedores de almacén

La propiedad MAPI **[PR_MDB_PROVIDER](pidtagstoreprovider-canonical-property.md)** especifica el GUID de un almacén de MAPI. Los GUID para los proveedores de almacén de que los índices de Outlook se describen en la siguiente tabla. 
  
||||
|:-----|:-----|:-----|
|**Tipo de proveedor de almacenamiento** <br/> |**GUID** <br/> |**Notas** <br/> |
|Archivos de carpetas personales (. (PST)  <br/> |{4154494E-BFF9-01B8-00AA-0037D96E0000}  <br/> |GUID se documenta en el mspst.h del archivo de encabezado público como **MSPST_UID_PROVIDER** <br/> |
|Exchange  <br/> |{C0A19454-7F29-1B10-A587-08002B2A2517}  <br/> |GUID se documenta en el edkmdb.h del archivo de encabezado público como **pbExchangeProviderPrimaryUserGuid** <br/> |
|Carpetas públicas  <br/> |{70fab278-f7af-cd11-9bc8-00aa002fc45a}  <br/> |GUID se documenta en el edkmdb.h del archivo de encabezado público como **pbExchangeProviderPublicGuid** <br/> |
|Outlook Connector para MSN  <br/> |{c34f5c97-eb05-bb4b-b199-2a7570ec7cf9}  <br/> |Ninguno  <br/> |
   
## <a name="see-also"></a>Vea también



[Información sobre la API del almacén](about-the-store-api.md)

