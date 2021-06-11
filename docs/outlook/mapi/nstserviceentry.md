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
ms.openlocfilehash: 96c04a242c477204ea1447fb78c31d189eeac59a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280057"
---
# <a name="nstserviceentry"></a>NSTServiceEntry

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Función de punto de entrada de servicio de mensajes para que un proveedor de almacén MAPI ajuste un almacén local basado en PST como almacén NST. 
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Implementado por:  <br/> |Proveedor MAPI  <br/> |
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

## <a name="parameters"></a>Parameters

 **NSTServiceEntry usa** el prototipo **[de función MSGSERVICEENTRY.](msgserviceentry.md)** Para obtener información sobre sus parámetros, vea **[MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="return-values"></a>Valores devueltos

Para obtener información sobre los valores devueltos, **[vea MSGSERVICEENTRY](msgserviceentry.md)**. 
  
## <a name="remarks"></a>Comentarios

Al usar **[GetProcAddress para](https://msdn.microsoft.com/library/ms683212.aspx)** buscar la dirección de esta función en msmapi32.dll, especifique "NSTServiceEntry" como nombre del procedimiento. 
  
Para usar la API de replicación, un proveedor de almacén MAPI primero debe abrir y ajustar un almacén local basado en PST llamando a **[NSTServiceEntry](nstserviceentry.md)**. A continuación, el proveedor puede usar las interfaces principales de la API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para llevar a cabo la replicación. 
  
Los siguientes comentarios se aplican a un almacén NST:
  
- No almacene ninguna información en la sección de perfil global al implementar un proveedor MAPI que use **NSTServiceEntry**. Muchos proveedores comparten la sección de perfil global y los datos almacenados en este perfil se pueden sobrescribir. 
    
- Solo los elementos con marcas de tiempo de modificación existentes obtienen sus marcas actualizadas cuando se guardan. 
    
- La comprobación de conflictos no se produce automáticamente cuando se guardan los elementos.
    
-  La detección de duplicados no se produce cuando se guardan los elementos. 
    
-  El archivo que representa la versión almacenada en caché del servidor se anexa con . NST. 
    
- Para obtener un puntero a la sección de perfil global, un servicio de mensajes llama a **[IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md)** en el objeto de soporte técnico mediante **pbNSTGlobalProfileSectionGuid** tal como se define a continuación: 
    
  ```
  #define  pbNSTGlobalProfileSectionGuid "\x85\xED\x14\x23\x9D\xF7\x42\x66\x8B\xF2\xFB\xD4\xA5\x21\x29\x41"
  ```

- En este caso, el objeto de soporte del servicio de mensajes debe asegurarse de que **IMAPISupport::OpenProfileSection** devuelve la sección de perfil identificada por la propiedad **[PR_SERVICE_UID](pidtagserviceuid-canonical-property.md)** en la sección de perfil predeterminada. Para obtener esta sección de perfil, el objeto de soporte puede abrir la sección de perfil predeterminada, recuperar PR_SERVICE_UID y pasar el resultado **a** **IMAPISupport::OpenProfileSection** para recuperar la sección de perfil global correcta. A su vez, el objeto de soporte devuelve un puntero a esta sección de perfil global al servicio de mensajes. 
    
## <a name="see-also"></a>Vea también



[Información sobre la API de replicación](about-the-replication-api.md)

