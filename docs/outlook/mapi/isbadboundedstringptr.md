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
ms.openlocfilehash: 39b4474bcc6bd71993fb5dc42bb2bfc1bf9f5f48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573407"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Comprueba que el proceso de llamada tiene acceso de lectura para el intervalo de memoria especificado.
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |mapiwin.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones de cliente y los proveedores de servicios.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Parámetros

 _lpsz_
  
> [entrada] Puntero a una cadena ASCII terminada en null.
    
 _cchMax_
  
> [entrada] El tamaño máximo de la cadena en caracteres. La función comprueba para acceso de lectura en todos los caracteres hasta el carácter null de terminación de la cadena o el número máximo de caracteres especificado por este parámetro, lo que sea menor. Si este parámetro es cero, el valor devuelto es cero.
    
## <a name="return-value"></a>Valor devuelto

El valor devuelto es cero cuando el proceso de llamada tiene acceso de lectura a todos los caracteres hasta el carácter null de terminación de la cadena o acceso de lectura hasta el número de caracteres especificado por _cchMax_.
  
El valor devuelto es distinto de cero cuando el proceso de llamada no tiene acceso de lectura a todos los caracteres hasta el carácter null de terminación de la cadena o acceso de lectura hasta el número de caracteres especificado por _cchMax_.
  
## <a name="remarks"></a>Comentarios

La función **IsBadBoundedStringPtr** equivale a usar **IsBadStringPtr**.
  
## <a name="see-also"></a>Recursos adicionales



[IsBadStringPtr](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

