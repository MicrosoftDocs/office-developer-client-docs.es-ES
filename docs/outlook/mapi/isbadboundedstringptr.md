---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278837"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba que el proceso de llamada tiene acceso de lectura al intervalo de memoria especificado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |mapiwin. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y aplicaciones cliente.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Parameters

 _lpsz_
  
> a Puntero a una cadena ASCII terminada en NULL.
    
 _cchMax_
  
> a Tamaño máximo de la cadena, en caracteres. La función comprueba el acceso de lectura en todos los caracteres hasta el carácter null de terminación de la cadena, o hasta el número de caracteres especificado por este parámetro, el que sea más pequeño. Si este parámetro es cero, el valor devuelto es cero.
    
## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero cuando el proceso de llamada tiene acceso de lectura a todos los caracteres hasta el carácter null de terminación de la cadena o acceso de lectura hasta el número de caracteres especificado por _cchMax_.
  
El valor devuelto es un valor distinto de cero cuando el proceso de llamada no tiene acceso de lectura a todos los caracteres hasta el carácter null de terminación de la cadena, o acceso de lectura hasta el número de caracteres especificado por _cchMax_.
  
## <a name="remarks"></a>Comentarios

La función **IsBadBoundedStringPtr** equivale a usar **IsBadStringPtr**.
  
## <a name="see-also"></a>Vea también



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

