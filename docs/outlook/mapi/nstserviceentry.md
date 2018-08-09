---
title: NSTServiceEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5ada6363-2406-4c0a-8326-a299a8bbefe1
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b5902c25197c2ae5790e654a8f29227e107b4a72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818420"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Hace referencia a**: Outlook 
  
Función de punto de entrada de servicio de mensajes para una MAPI proveedor para ajustar un almacén local basada en PST como un almacén de NST de almacén. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Se implementa mediante:  <br/> |Proveedor MAPI  <br/> |
|Llamado por:  <br/> |MAPI  <br/> |
   
```cpp
HRESULT NSTServiceEntry( 
    HINSTANCE hInstance,   
    LPMALLOC lpMalloc, 
    LPMAPISUP lpMAPISup, 
    ULONG ulUIParam, 
    ULONG ulFlags, 
    ULONG ulContext, 
    ULONG cValues, 
    LPSPropValue lpProps, 
    LPPROVIDERADMIN lpProviderAdmin, 
    LPMAPIERROR FAR * lppMapiError 
);
```

## <a name="parameters"></a>Parámetros

 **NSTServiceEntry** utiliza el prototipo de función **[MSGSERVICEENTRY](msgserviceentry.md)** . Para obtener información sobre sus parámetros, consulte **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Valores devueltos

Para obtener información acerca de los valores devueltos, vea **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Comentarios

Cuando se usa **[GetProcAddress](http://msdn.microsoft.com/en-us/library/ms683212.aspx)** para buscar la dirección de esta función en msmapi32.dll, especifique "NSTServiceEntry" como el nombre del procedimiento. 
  
Para usar la API de replicación, un proveedor de almacén MAPI en primer lugar debe abrir y se ajusta a un almacén local basada en PST mediante una llamada a **[NSTServiceEntry](nstserviceentry.md)**. El proveedor, a continuación, puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** y **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación. 
  
Los siguientes comentarios son aplicables a un almacén de NST:
  
- No almacene ninguna información en la sección perfil global al implementar un proveedor MAPI que usa **NSTServiceEntry**. La sección de perfil global es compartida por muchos de los proveedores y se pueden sobrescribir los datos almacenados en este perfil. 
    
- Sólo los elementos con marcas de hora de modificación existente obtienen sus marcas que se actualizan cuando se guardan. 
    
- Comprobación de conflictos no se producen automáticamente cuando se guardan los elementos.
    
-  Detección de duplicados no se produce cuando se guardan los elementos. 
    
-  Se agrega el archivo que representa la versión almacenada en caché del servidor. NST. 
    
- Para obtener un puntero a la sección de perfil global, un servicio de mensajes llama a **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** en el objeto de soporte técnico mediante **pbNSTGlobalProfileSectionGuid** tal como se define a continuación: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- En este caso, el objeto de soporte técnico del servicio de mensajes debe asegurarse de que **IMAPISupport::OpenProfileSection** devuelve la sección de perfil que se identifica con la propiedad **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** en la sección de perfil predeterminado. Para obtener esta sección de perfil, el objeto de soporte técnico puede abrir la sección de perfil predeterminado, recuperar **PR_SERVICE_UID**y pasa el resultado a **IMAPISupport::OpenProfileSection** para recuperar la sección de perfil global correcto. El objeto de soporte a su vez devuelve un puntero a esta sección de perfil global para el servicio de mensajes. 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)

