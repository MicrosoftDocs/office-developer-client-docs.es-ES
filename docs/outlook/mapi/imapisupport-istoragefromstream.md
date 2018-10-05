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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392833"
---
# <a name="imapisupportistoragefromstream"></a>IMAPISupport::IStorageFromStream

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Implementa un objeto de almacenamiento para obtener acceso a una secuencia.
  
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
  
> [entrada] Un puntero a un objeto stream.
    
 _lpInterface_
  
> [entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso a la secuencia indicada por _lpUnkIn_. Cualquiera de los valores siguientes son válido: IID_IStream, IID_ILockBytes, o **null**, que indica que debe usarse la interfaz [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) para tener acceso a la secuencia. 
    
 _ulFlags_
  
> [entrada] Una máscara de bits de indicadores que controla cómo es el objeto de almacenamiento que se creará en relación con el objeto stream. De forma predeterminada, se crea el almacenamiento con acceso de solo lectura y se inicia la secuencia en la posición cero en el almacenamiento de información. Se pueden establecer los siguientes indicadores:
    
STGSTRM_CREATE 
  
> Para el objeto stream, se debe crear un nuevo objeto de almacenamiento.
    
STGSTRM_CURRENT 
  
> El objeto de almacenamiento debe comenzar en la posición actual de la secuencia.
    
STGSTRM_MODIFY 
  
> El llamador debe tener permiso de lectura y escritura para el objeto de almacenamiento devuelto.
    
STGSTRM_RESET 
  
> El objeto de almacenamiento debe comenzar en la posición cero.
    
 _lppStorageOut_
  
> [out] Un puntero a un puntero al objeto de almacenamiento.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> Se ha creado correctamente el objeto de almacenamiento.
    
## <a name="remarks"></a>Comentarios

El método **IMAPISupport::IStorageFromStream** se implementa para todos los objetos de soporte técnico de proveedor de servicio. Proveedores de servicios de llamar a **IStorageFromStream** para crear un objeto de almacenamiento que se usará para abrir propiedades concretas. Proveedores de servicios que tienen su propia implementación de la interfaz [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) no es necesario llamar a **IStorageFromStream**. 
  
El objeto de almacenamiento creado por **IStorageFromStream** llama al método [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) de la secuencia para incrementar su recuento de referencia y, a continuación, se disminuye el recuento cuando se libera el almacenamiento. 
  
## <a name="notes-to-callers"></a>Notas para los llamadores

Cuando se llama al método de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de uno de los objetos para abrir una propiedad con la interfaz **IStorage** , realice las siguientes tareas: 
  
1. Abrir un objeto stream con el permiso de lectura y escritura para la propiedad.
    
2. Internamente, marque la secuencia de la propiedad como un objeto de almacenamiento.
    
3. Llame a **IStorageFromStream** para generar un objeto de almacenamiento. 
    
4. Devolver un puntero a este objeto de almacenamiento.
    
Si implementa interfaces adicionales que utilizan el objeto de almacenamiento, cree un objeto que encapsula el objeto de almacenamiento e implementar un método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de nivel superior. 
  
No permitir una propiedad para abrirse con la interfaz **IStream** si se creó con **IStorage**. Por el contrario, no permitir una propiedad para abrirse con la interfaz **IStorage** si se creó con **IStream**. 
  
Con una excepción, es aceptable para usar la interfaz de **IStreamDocfile** para un objeto de almacenamiento de un contenedor a otro en secuencia, pero se debe pasar el identificador de interfaz IID_IStreamDocfile en el método de **OpenProperty** _lpInterface _parámetro. 
  
## <a name="see-also"></a>Vea también



[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

