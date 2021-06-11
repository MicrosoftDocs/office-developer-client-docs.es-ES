---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9b11b134f5d4a32a5a55008f557821d74b474bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429568"
---
# <a name="mapioffline_createinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Esta estructura se usa con [HrCreateOfflineObj](hrcreateofflineobj.md).
  
```cpp
typedef struct
{
  ULONG      ulSize;
  ULONG      ulCreateFlags;
  LPCWSTR      pwszProfileName;
  ULONG      ulCapabilities;
  const GUID*      pGUID;
  const GUID*      pInstance;
  IMAPIOfflineMgr*    pParent;
  IUnknown*      pMAPISupport;
  MAPIOFFLINE_AGGREGATEINFO*  pAggregateInfo;
  MAPIOFFLINE_CONNECTINFO*  pConnectInfo;
} MAPIOFFLINE_CREATEINFO;
```

## <a name="members"></a>Members

 **ulSize**
  
> El tamaño de la estructura.
    
 **ulCreateFlags**
  
> Debe ser 0.
    
 **pwszProfileName**
  
> Nombre del perfil.
    
 **ulCapabilities**
  
> Máscara de bits de las siguientes marcas de funcionalidad.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |El objeto sin conexión es capaz de desconectarse.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |El objeto sin conexión es capaz de ponerse en línea.  <br/> |
   
 **pGUID**
  
> Puntero a un GUID que se usa para identificar de forma única este tipo de objeto sin conexión desde otros objetos sin conexión. GUID_GlobalState hace referencia al objeto sin conexión global que los objetos pueden usar como objeto primario.
    
 **pInstance**
  
> Puntero al GUID que identifica de forma exclusiva este objeto sin conexión. Se usa para desambiguar estos objetos sin conexión de otros objetos.
    
 **pParent**
  
> Puntero al objeto sin conexión que es el elemento primario de este objeto sin conexión y cuyos cambios heredará este objeto sin conexión.
    
 **pMAPISupport**
  
>  Identifica el objeto de soporte técnico MAPI que usará este objeto sin conexión. Por ejemplo, si este objeto sin conexión se usa para realizar un seguimiento del estado sin conexión y en línea de un almacén, este es el objeto de soporte de almacenes. Sin embargo, si se trata de un objeto sin conexión para un objeto sin ningún objeto de soporte, puede ser NULL. 
    
 **pAggregateInfo**
  
> Puntero a una MAPIOFFLINE_AGGREGATEINFO estructura. Para obtener más información, [vea MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Debe ser null.
    
## <a name="see-also"></a>Vea también



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

