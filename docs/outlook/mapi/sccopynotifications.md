---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435925"
---
# <a name="sccopynotifications"></a>ScCopyNotifications

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Copia un grupo de notificaciones de eventos en un único bloque de memoria. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Aplicaciones cliente y proveedores de servicios  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a>Parameters

 _CNTF_
  
> a Número de estructuras de [notificación](notification.md) en la matriz indicada por el parámetro _rgntf_ . 
    
 _rgntf_
  
> a Puntero a una matriz de estructuras de **notificación** que define las notificaciones de eventos que se van a copiar. 
    
 _pvDst_
  
> contempla Puntero a las notificaciones devueltas. 
    
 _impreso_
  
> contempla Puntero opcional a una variable en la que se almacena el tamaño, en bytes, de la matriz señalada por el parámetro _rgntf_ . Si no es NULL, el parámetro _PCB_ se establece en el número de bytes almacenados en el parámetro _pvDst_ . 
    
## <a name="return-value"></a>Valor devuelto

S_OK
  
> Las notificaciones de eventos se han copiado correctamente.
    
E_INVALIDARG
  
> Se encontró una notificación no válida.
    
## <a name="remarks"></a>Comentarios

Si se pasa NULL en el parámetro _PCB_ , no se realiza ninguna copia; Si se pasa un valor no NULL en _PCB_, la función **ScCopyNotifications** copia el tamaño de la matriz y la matriz en sí a un bloque de memoria único. Si _PCB_ no es null, se establece en el número de bytes almacenados en el parámetro _pvDst_ . El parámetro _pvDst_ debe ser lo suficientemente grande como para contener toda la matriz. 
  

