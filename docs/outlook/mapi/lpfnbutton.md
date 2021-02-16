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
ms.openlocfilehash: 804bd23a148b942fd4580d1e3465fc1f65ff5978
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431515"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada a la que MAPI llama para activar un control de botón opcional en un cuadro de diálogo de libreta de direcciones. Este botón suele ser **un botón Detalles.** 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs.h  <br/> |
|Función definida implementada por:  <br/> |Proveedores de servicios  <br/> |
|Función definida llamada por:  <br/> |MAPI  <br/> |
   
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
  
> [entrada] Identificador de las ventanas primarias para los cuadros de diálogo o ventanas que muestra esta función.
    
 _lpvContext_
  
> [entrada] Puntero a un valor arbitrario pasado a la función de devolución de llamada cuando MAPI lo llama. Este valor puede representar una dirección significativa para la aplicación cliente. Normalmente, para el código C++,  _lpvContext representa_ un puntero a un objeto C++. 
    
 _cbEntryID_
  
> [entrada] Tamaño, en bytes, del identificador de entrada al que apunta el _parámetro lpSelection._ 
    
 _lpSelection_
  
> [entrada] Puntero al identificador de entrada que define la selección en el cuadro de diálogo.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman a una función de devolución de llamada basada en el **prototipo LPFNBUTTON** para definir un botón en un cuadro de diálogo de detalles. El cliente pasa un puntero a la función de devolución de llamada en llamadas al método [IAddrBook::D etails.](iaddrbook-details.md) 
  
Los proveedores de servicios llaman a una función de enlace basada en el **prototipo LPFNBUTTON** para definir un botón en un cuadro de diálogo de detalles. El proveedor pasa un puntero a esta función de enlace en llamadas al método [IMAPISupport::D etails.](imapisupport-details.md) 
  
En ambos casos, cuando se muestra el cuadro de diálogo y el usuario elige el botón definido, MAPI llama **a LPFNBUTTON**. 
  
## <a name="see-also"></a>Consulte también



[BuildDisplayTable](builddisplaytable.md)

