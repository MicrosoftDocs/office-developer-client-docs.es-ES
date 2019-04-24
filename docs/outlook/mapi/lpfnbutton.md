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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357445"
---
# <a name="lpfnbutton"></a>LPFNBUTTON

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Define una función de devolución de llamada que MAPI llama para activar un control de botón opcional en un cuadro de diálogo de la libreta de direcciones. Normalmente, este botón es un botón **detalles** . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapidefs. h  <br/> |
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

## <a name="parameters"></a>Parameters

 _ulUIParam_
  
> a Identificador de las ventanas primarias de los cuadros de diálogo o ventanas que muestra la función.
    
 _lpvContext_
  
> a Puntero a un valor arbitrario que se pasa a la función de devolución de llamada cuando MAPI la llama. Este valor puede representar una dirección de importancia para la aplicación cliente. Normalmente, para código de C++, _lpvContext_ representa un puntero a un objeto de c++. 
    
 _cbEntryID_
  
> a Tamaño, en bytes, del identificador de entrada al que apunta el parámetro _lpSelection_ . 
    
 _lpSelection_
  
> a Puntero al identificador de entrada que define la selección en el cuadro de diálogo.
    
 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente llaman a una función de devolución de llamada basada en el prototipo **LPFNBUTTON** para definir un botón en un cuadro de diálogo de detalles. El cliente pasa un puntero a la función de devolución de llamada en llamadas al método [IAddrBook::D etails](iaddrbook-details.md) . 
  
Los proveedores de servicios llaman a una función de enlace en función del prototipo **LPFNBUTTON** para definir un botón en un cuadro de diálogo de detalles. El proveedor pasa un puntero a esta función de enlace en las llamadas al método [IMAPISupport::D etails](imapisupport-details.md) . 
  
En ambos casos, cuando se muestra el cuadro de diálogo y el usuario elige el botón definido, llamadas MAPI **LPFNBUTTON**. 
  
## <a name="see-also"></a>Vea también



[BuildDisplayTable](builddisplaytable.md)

