---
title: IAddrBookGetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.GetDefaultDir
api_type:
- COM
ms.assetid: 7a9fdf3f-fd76-40fb-8217-967c6efba5f6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7309f65965fe3c88f927eeba0bbcccff97c479af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817137"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Hace referencia a**: Outlook 
  
Devuelve el identificador de entrada para el contenedor de la libreta de direcciones inicial.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpcbEntryID_
  
> [out] Un puntero para el número de bytes en el identificador de entrada indicado por el parámetro _lppEntryID_ . 
    
 _lppEntryID_
  
> [out] Un puntero a un puntero al identificador de entrada del contenedor predeterminado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada del contenedor predeterminado se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

Proveedores de servicios y aplicaciones cliente de llamar al método **GetDefaultDir** para recuperar el identificador de entrada del contenedor de la libreta de direcciones predeterminada. El contenedor predeterminado es lo que ve el usuario que se muestra en la libreta de direcciones cuando se abre por primera vez la libreta de direcciones. Si no se ha establecido un contenedor predeterminado mediante una llamada al método [IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md) , MAPI asigna como el contenedor predeterminado del primer contenedor con nombres que no es la libreta de direcciones personales (PAB). Si no se encuentra un contenedor de este tipo, el archivo PAB se convierte en el contenedor predeterminado. 
  
Para establecer el valor predeterminado Active directory, un cliente o proveedor llama al método de **SetDefaultDir** . Los clientes y proveedores no es necesario llamar al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ; debido a que los cambios realizados en la libreta de direcciones no se negocian, cambios se realizan inmediatamente permanentes. 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI usa el método **GetDefaultDir** para obtener el identificador para el contenedor de la libreta de direcciones predeterminada.  <br/> |
   
## <a name="see-also"></a>Vea también



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

