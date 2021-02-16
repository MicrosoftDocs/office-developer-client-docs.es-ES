---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316595"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Implementa un objeto de almacenamiento para tener acceso a una secuencia.
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a>Parámetros

 _lpUnkIn_
  
> [entrada] Puntero a un objeto de secuencia.
    
 _lpInterface_
  
> [entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la secuencia a la que apunta  _lpUnkIn_. Cualquiera de los siguientes valores son válidos: IID_IStream, IID_ILockBytes o **null**, lo que indica que se debe usar la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para obtener acceso a la secuencia. 
    
 _ulFlags_
  
> [entrada] Máscara de bits de marcas que controla cómo se va a crear el objeto de almacenamiento en relación con el objeto de secuencia. De forma predeterminada, el almacenamiento se crea con acceso de solo lectura y la secuencia comienza en la posición cero del almacenamiento. Se pueden establecer las siguientes marcas:
    
STGSTRM_CREATE 
  
> Se debe crear un nuevo objeto de almacenamiento para el objeto de secuencia.
    
STGSTRM_CURRENT 
  
> El objeto de almacenamiento debe comenzar en la posición actual de la secuencia.
    
STGSTRM_MODIFY 
  
> El autor de la llamada debe tener permiso de lectura y escritura para el objeto de almacenamiento devuelto.
    
STGSTRM_RESET 
  
> El objeto de almacenamiento debe comenzar en la posición cero.
    
 _lppStorageOut_
  
> [salida] Puntero a un puntero al objeto de almacenamiento.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El objeto de almacenamiento se creó correctamente.
    
## <a name="remarks"></a>Comentarios

El **método IMAPISupport::IStorageFromStream** se implementa para todos los objetos de compatibilidad del proveedor de servicios. Los proveedores de servicios **llaman a IStorageFromStream** para crear un objeto de almacenamiento que se usará para abrir propiedades concretas. Los proveedores de servicios que tienen su propia implementación de [la interfaz IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) no necesitan llamar a **IStorageFromStream**. 
  
El objeto de almacenamiento creado por **IStorageFromStream** llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) de la secuencia para incrementar su recuento de referencias y, a continuación, disminuye el recuento cuando se libera el almacenamiento. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se llama al método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de uno de los objetos para abrir una propiedad con la interfaz **IStorage,** realice las siguientes tareas: 
  
1. Abra un objeto de secuencia con permiso de lectura y escritura para la propiedad.
    
2. Marca internamente la secuencia de propiedades como un objeto de almacenamiento.
    
3. Llama **a IStorageFromStream** para generar un objeto de almacenamiento. 
    
4. Devuelve un puntero a este objeto de almacenamiento.
    
Si implementa interfaces adicionales que usan el objeto de almacenamiento, cree un objeto que ajuste el objeto de almacenamiento e implemente un método [IUnknown::QueryInterface de nivel](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) superior. 
  
No permitir que se abra una propiedad con la **interfaz IStream** si se creó con **IStorage**. Por el contrario, no permita que se abra una propiedad con la interfaz **IStorage** si se creó con **IStream**. 
  
Con una excepción, es aceptable usar la interfaz **IStreamDocfile** para transmitir un objeto de almacenamiento de un contenedor a otro, pero el identificador de interfaz IID_IStreamDocfile debe pasarse en el parámetro _lpInterface_ del método **OpenProperty.** 
  
## <a name="see-also"></a>Consulte también



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

