---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346665"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Libera un búfer de memoria asignado con una llamada a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) o a la función [MAPIAllocateMore](mapiallocatemore.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parameters

 _lpBuffer_
  
> a Puntero a un búfer de memoria asignado previamente. Si se pasa NULL en el parámetro _lpBuffer_ , **MAPIFreeBuffer** no realiza ninguna acción. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se realizó correctamente y liberó la memoria solicitada. **MAPIFreeBuffer** también puede devolver S_OK en ubicaciones ya libres o si el bloque de memoria no se asigna con **MAPIAllocateBuffer** y **MAPIAllocateMore**.
    
## <a name="remarks"></a>Comentarios

Normalmente, cuando una aplicación cliente o un proveedor de servicios llaman a [MAPIAllocateBuffer](mapiallocatebuffer.md) o [MAPIAllocateMore](mapiallocatemore.md), el sistema operativo construye un búfer de memoria contiguo una o más estructuras complejas con varios niveles de punteros. Cuando una función o un método MAPI crea un búfer con este contenido, un cliente puede liberar más adelante todas las estructuras contenidas en el búfer pasando a **MAPIFreeBuffer** el puntero al búfer devuelto por la función MAPI que ha creado el búfer. Para que un proveedor de servicios libere un búfer de memoria mediante **MAPIFreeBuffer**, debe pasar el puntero a ese búfer devuelto con el objeto support del proveedor. 
  
La llamada a **MAPIFreeBuffer** para liberar un búfer determinado debe realizarse en cuanto un cliente o proveedor termine de usar este búfer. La simple llamada al método [IMAPISession:: Logoff](imapisession-logoff.md) al final de una sesión MAPI no libera automáticamente los búferes de memoria. 
  
Un cliente o proveedor de servicios debe actuar por el supuesto de que el puntero pasado en _lpBuffer_ no es válido después de una devolución correcta de **MAPIFreeBuffer**. Si el puntero indica un bloque de memoria no asignado por el sistema de mensajería mediante **MAPIAllocateBuffer** o **MAPIAllocateMore** o un bloque de memoria libre, el comportamiento de **MAPIFreeBuffer** no está definido. 
  
> [!NOTE]
> Pasar un puntero nulo a **MAPIFreeBuffer** simplifica y reduce el código de limpieza de la aplicación porque **MAPIFreeBuffer** puede inicializar punteros a NULL y, a continuación, liberarlos en el código de limpieza sin tener que probarlos primero. 
  
## <a name="see-also"></a>Vea también



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

