---
title: MAPIUninitialize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIUninitialize
api_type:
- HeaderDef
ms.assetid: 0f4e54dc-80e5-49a7-9703-0225d8133492
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c1a78889ea98133af46089fdc93b0c1c4bb24226
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818300"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Hace referencia a**: Outlook 
  
Disminuye el recuento de referencia, limpia y elimina por instancia global de datos para la DLL de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Parámetros

Ninguno 
  
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Una aplicación cliente llama a la función **MAPIUninitialize** para finalizar su interacción con MAPI, comenzado con una llamada a la función [MAPIInitialize](mapiinitialize.md) . Después de llamar a **MAPIUninitialize** , no hay otras llamadas MAPI pueden estar por el cliente. 
  
 **MAPIUninitialize** disminuye el recuento de referencia, y la función **MAPIInitialize** correspondiente incrementa el recuento de referencia. Por lo tanto, el número de llamadas a una función debe ser igual que el número de llamadas a otro. 
  
> [!NOTE]
> No se puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función de Win32 **DllMain** o cualquier otra función que crea o termina subprocesos. Para obtener más información, vea [Uso de objetos de subprocesos](using-thread-safe-objects.md). 
  

