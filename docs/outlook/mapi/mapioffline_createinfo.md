---
title: MAPIOFFLINE_CREATEINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 539aa31d-7dec-4dbb-93f7-fa060c43565a
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 17ab26c62bcbb57ff8e53b5412ca27ed414fb725
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818265"
---
# <a name="mapiofflinecreateinfo"></a>MAPIOFFLINE_CREATEINFO

  
  
**Se aplica a**: Outlook 
  
Esta estructura se utiliza con [HrCreateOfflineObj](hrcreateofflineobj.md).
  
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

## <a name="members"></a>Miembros

 **ulSize**
  
> El tamaño de la estructura.
    
 **ulCreateFlags**
  
> Debe ser 0.
    
 **pwszProfileName**
  
> Nombre del perfil.
    
 **ulCapabilities**
  
> Una máscara de bits de los siguientes indicadores de capacidad.
    
|||
|:-----|:-----|
|MAPIOFFLINE_CAPABILITY_OFFLINE  <br/> |El objeto sin conexión es capaz de trabajar sin conexión.  <br/> |
|MAPIOFFLINE_CAPABILITY_ONLINE  <br/> |El objeto sin conexión es capaz de conectarse.  <br/> |
   
 **pGUID**
  
> Puntero a un GUID que se utiliza para identificar de forma exclusiva este tipo de objeto sin conexión desde otros objetos sin conexión. GUID_GlobalState hace referencia al objeto global sin conexión que los objetos pueden usar como un objeto primario.
    
 **pInstance**
  
> Puntero al GUID que identifica de forma exclusiva este objeto sin conexión. Se usa para eliminar la ambigüedad de esta objetos sin conexión desde otros objetos.
    
 **pParent**
  
> Puntero al objeto sin conexión que es el elemento primario de este objeto sin conexión y cuyos cambios heredará este objeto sin conexión.
    
 **pMAPISupport**
  
>  Identifica el objeto de soporte técnico MAPI que usará este objeto sin conexión. Por ejemplo, si este objeto sin conexión se usa para realizar un seguimiento de un almacén sin conexión y el estado en línea, a continuación, esto es los almacenes admiten el objeto. Sin embargo, si se trata de un objeto sin conexión para un objeto con ningún objeto de soporte técnico, a continuación, puede ser NULL. 
    
 **pAggregateInfo**
  
> Un puntero a una estructura MAPIOFFLINE_AGGREGATEINFO. Para obtener más información, vea [MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md).
    
 **pConnectInfo**
  
> Debe ser null.
    
## <a name="see-also"></a>Ver también



[HrCreateOfflineObj](hrcreateofflineobj.md)
  
[MAPIOFFLINE_AGGREGATEINFO](mapioffline_aggregateinfo.md)

