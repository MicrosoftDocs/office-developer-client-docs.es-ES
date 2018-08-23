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
ms.openlocfilehash: ad3d9d12e1073610747b0ab078c6d65c09f8c7c1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569144"
---
# <a name="mapifreebuffer"></a>MAPIFreeBuffer

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Libera un búfer de memoria asignado con una llamada a la función [MAPIAllocateBuffer](mapiallocatebuffer.md) o la función [MAPIAllocateMore](mapiallocatemore.md) . 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapix.h  <br/> |
|Se implementa mediante:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Las aplicaciones cliente y los proveedores de servicios  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a>Parámetros

 _lpBuffer_
  
> [entrada] Puntero a un búfer de memoria previamente asignado. Si se pasa NULL en el parámetro _lpBuffer_ , **MAPIFreeBuffer** no tiene ningún efecto. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y libera la memoria solicitada. **MAPIFreeBuffer** también puede devolver S_OK en ubicaciones ya liberadas o si no se asigna el bloque de memoria con **MAPIAllocateBuffer** y **MAPIAllocateMore**.
    
## <a name="remarks"></a>Comentarios

Normalmente, cuando una aplicación de cliente o un proveedor de servicios llama a [MAPIAllocateBuffer](mapiallocatebuffer.md) o [MAPIAllocateMore](mapiallocatemore.md), las construcciones de sistema operativo en el búfer de memoria contigua uno uno o más estructuras complejas con varios niveles de punteros. Cuando una función de MAPI o un método crea un búfer con dicho contenido, un cliente más adelante puede liberar todas las estructuras contenidas en el búfer, se pasa al **MAPIFreeBuffer** el puntero en el búfer devuelto por la función MAPI que creó el búfer. Para que un proveedor de servicios liberar un búfer de memoria mediante **MAPIFreeBuffer**, debe pasar el puntero a ese búfer devuelto con objeto de soporte técnico del proveedor. 
  
La llamada a **MAPIFreeBuffer** para liberar un búfer determinado se debe realizar tan pronto como un cliente o proveedor haya terminado de usar este búfer. Simplemente la llamada al método [IMAPISession::Logoff](imapisession-logoff.md) al final de una sesión MAPI, búferes de memoria no libera automáticamente. 
  
Un proveedor de cliente o servicio debe funcionar en la suposición de que el puntero se pasan en _lpBuffer_ no es válido después de una devolución de **MAPIFreeBuffer**es correcta. Si el puntero indica un bloque de memoria no asignado por el sistema de mensajería a través de **MAPIAllocateBuffer** o **MAPIAllocateMore** o un bloque de memoria libre, el comportamiento de **MAPIFreeBuffer** no está definido. 
  
> [!NOTE]
> Pasar un puntero nulo a **MAPIFreeBuffer** hace que código de limpieza de la aplicación más sencilla y más pequeño porque **MAPIFreeBuffer** puede inicializar punteros a NULL y, a continuación, liberarlos en el código de limpieza sin tener que volver a probarlas en primer lugar. 
  
## <a name="see-also"></a>Recursos adicionales



[IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md)

