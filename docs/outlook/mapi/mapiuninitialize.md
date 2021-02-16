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
ms.openlocfilehash: f7339588bcc6815545e7341eafffe9cf001c1d76
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408526"
---
# <a name="mapiuninitialize"></a>MAPIUninitialize

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Disminuye el recuento de referencias, limpia y elimina los datos globales por instancia para la DLL de MAPI. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente  <br/> |
   
```cpp
void MAPIUninitialize ( void );
```

## <a name="parameters"></a>Parámetros

Ninguno 
  
## <a name="return-value"></a>Valor devuelto

Ninguno.
  
## <a name="remarks"></a>Comentarios

Una aplicación cliente llama a la **función MAPIUninitialize** para finalizar su interacción con MAPI, iniciada con una llamada a la [función MAPIInitialize.](mapiinitialize.md) Después **de llamar a MAPIUninitialize,** el cliente no puede realizar ninguna otra llamada MAPI. 
  
 **MAPIUninitialize** disminuye el recuento de referencias y la función **MAPIInitialize** correspondiente incrementa el recuento de referencias. Por lo tanto, el número de llamadas a una función debe ser igual al número de llamadas a la otra. 
  
> [!NOTE]
> No puede llamar a **MAPIInitialize** o **MAPIUninitialize** desde dentro de una función **DllMain** de Win32 o cualquier otra función que cree o finalice subprocesos. Para obtener más información, vea [Utilizar Thread-Safe objetos](using-thread-safe-objects.md). 
  

