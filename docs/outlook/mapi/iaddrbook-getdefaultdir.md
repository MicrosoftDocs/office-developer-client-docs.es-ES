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
ms.openlocfilehash: d9ad74d8ae02a49ee3c222394caedfd571f84b1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436877"
---
# <a name="iaddrbookgetdefaultdir"></a>IAddrBook::GetDefaultDir

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Devuelve el identificador de entrada del contenedor de la libreta de direcciones inicial.
  
```cpp
HRESULT GetDefaultDir(
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a>Parámetros

 _lpcbEntryID_
  
> [salida] Puntero al recuento de bytes en el identificador de entrada al que apunta el _parámetro lppEntryID._ 
    
 _lppEntryID_
  
> [salida] Puntero a un puntero al identificador de entrada del contenedor predeterminado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El identificador de entrada del contenedor predeterminado se devolvió correctamente.
    
## <a name="remarks"></a>Comentarios

Las aplicaciones cliente y los proveedores de servicios llaman al **método GetDefaultDir** para recuperar el identificador de entrada del contenedor de libreta de direcciones predeterminado. El contenedor predeterminado es lo que el usuario ve que se muestra en la libreta de direcciones cuando se abre la libreta de direcciones por primera vez. Si no se ha establecido un contenedor predeterminado mediante una llamada al método [IAddrBook::SetDefaultDir,](iaddrbook-setdefaultdir.md) MAPI asigna como contenedor predeterminado el primer contenedor con nombres que no son la libreta de direcciones personal (PAB). Si no se encuentra este contenedor, el PAB se convierte en el contenedor predeterminado. 
  
Para establecer el directorio predeterminado, un cliente o proveedor llama al **método SetDefaultDir.** Los clientes y proveedores no tienen que llamar al [método IMAPIProp::SaveChanges;](imapiprop-savechanges.md) dado que los cambios en la libreta de direcciones no se realizan, los cambios se realizan inmediatamente de forma permanente. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnOpenDefaultDir  <br/> |MFCMAPI usa el **método GetDefaultDir** para obtener el identificador del contenedor de libreta de direcciones predeterminado.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IAddrBook::SetDefaultDir](iaddrbook-setdefaultdir.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[Propiedad canónica PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

