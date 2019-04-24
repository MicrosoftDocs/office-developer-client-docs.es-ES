---
title: GetTnefStreamCodepage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f22ccf2-1004-4731-9d68-f66c01b4588b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1e3d384f35726ff28bb47f3d537c8a7a1dda6dce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299436"
---
# <a name="gettnefstreamcodepage"></a>GetTnefStreamCodepage

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Determina la página de códigos de una secuencia de formato de encapsulación neutro para el transporte (TNEF).
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |TNEF. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y aplicaciones cliente.  <br/> |
   
```cpp
HRESULT GetTnefStreamCodepage(
  LPSTREAM lpStream,
  ULONG FAR * lpulCodepage,
  ULONG FAR * lpulSubCodepage
);
```

## <a name="parameters"></a>Parameters

 _lpStream_
  
> a Puntero a una interfaz OLE **IStream** del objeto de la secuencia de almacenamiento que proporciona un origen para un mensaje de transmisión TNEF. 
    
 _lpulCodepage_
  
> contempla Puntero a la página de códigos del objeto Stream.
    
 _lpulSubCodepage_
  
> contempla Puntero a la página de subcódigo del objeto Stream.
    
## <a name="return-value"></a>Valor devuelto

 **S_OK**
  
> La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.
    
 **MAPI_E_NOT_ENOUGH_DISK**
  
> Error al leer un atributo en la secuencia TNEF.
    
 **MAPI_E_CORRUPT_DATA**
  
> La secuencia no era una secuencia TNEF o hubo un error al leer el atributo attOemCodepage.
    
## <a name="remarks"></a>Comentarios

Utilice la función **GetTnefStreamCodepage** para leer el atributo **attOemCodepage** de la secuencia TNEF y determinar la página de códigos y la página de subcódigo. Si no se encuentra **attOemCodepage** , **GetTnefStreamCodepage** devuelve una página de códigos de 437 y una página de subcódigo de 0. 
  
## <a name="see-also"></a>Vea también



[attOemCodepage](https://msdn.microsoft.com/library/ee158667%28EXCHG.80%29.aspx)

