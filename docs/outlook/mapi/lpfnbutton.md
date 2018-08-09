---
title: LPFNBUTTON
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.LPFNBUTTON
api_type:
- COM
ms.assetid: cb91ae1d-1ea8-4f02-a1f1-f2a356a71477
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e1f15a5f031f5c5a9568b8a36722eaac011b814c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818033"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Hace referencia a**: Outlook 
  
Define una función de devolución de llamada que llama MAPI para activar un control de botón opcional en un cuadro de diálogo de la libreta de direcciones. Normalmente, este botón es un botón de **Detalles** . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definido implementada por:  <br/> |Proveedores de servicios  <br/> |
|Llamado por una función definida:  <br/> |MAPI  <br/> |
   
```cpp
SCODE (STDMETHODCALLTYPE FAR * LPFNBUTTON)(
  ULONG_PTR ulUIParam,
  LPVOID lpvContext,
  ULONG cbEntryID,
  LPENTRYID lpSelection,
  ULONG ulFlags
);
```

## <a name="parameters"></a>Parámetros

 _ulUIParam_
  
> [entrada] Controlador de las ventanas de primario para todos los cuadros de diálogo o windows que muestra esta función.
    
 _lpvContext_
  
> [entrada] Puntero a un valor arbitrario se pasa a la función de devolución de llamada cuando llama a MAPI. Este valor puede representar una dirección de importancia a la aplicación cliente. Normalmente, para el código de C++, _lpvContext_ representa un puntero a un objeto de C++. 
    
 _cbEntryID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada que señala el parámetro _lpSelection_ . 
    
 _lpSelection_
  
> [entrada] Puntero a la definición de la selección en el cuadro de diálogo de identificador de entrada.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente de llamar a una función de devolución de llamada según el prototipo **LPFNBUTTON** para definir un botón en un cuadro de diálogo detalles. El cliente pasa un puntero a la función de devolución de llamada en las llamadas al método [IAddrBook::Details](iaddrbook-details.md) . 
  
Proveedores de servicios de llamar a una función de enlace según el prototipo **LPFNBUTTON** para definir un botón en un cuadro de diálogo detalles. El proveedor pasa un puntero a esta función de enlace en las llamadas al método [IMAPISupport::Details](imapisupport-details.md) . 
  
En ambos casos, cuando se muestra el cuadro de diálogo y el usuario elige el botón definido, MAPI llama **LPFNBUTTON**. 
  
## <a name="see-also"></a>Vea también



[BuildDisplayTable](builddisplaytable.md)

