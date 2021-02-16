---
title: IAddrBookSetDefaultDir
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IAddrBook.SetDefaultDir
api_type:
- COM
ms.assetid: d5d60150-15e4-41ff-bfb0-0c67e2abcacc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ab01f189734ac30b4c027f4e5596c88031b5f99
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341702"
---
# <a name="iaddrbooksetdefaultdir"></a>IAddrBook::SetDefaultDir

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Establece el contenedor especificado como contenedor de libreta de direcciones predeterminado.
  
```cpp
HRESULT SetDefaultDir(
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parámetros

 _cbEntryID_
  
> [entrada] Recuento de bytes en el identificador de entrada al que apunta el _parámetro lpEntryID._ 
    
 _lpEntryID_
  
> [entrada] Puntero al identificador de entrada del contenedor de libreta de direcciones predeterminado.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> El contenedor de libreta de direcciones predeterminado se estableció correctamente.
    
## <a name="remarks"></a>Comentarios

Los clientes y proveedores de servicios llaman **al método SetDefaultDir** para establecer un nuevo contenedor de libreta de direcciones predeterminado. El contenedor predeterminado es el contenedor que el usuario ve que se muestra en la libreta de direcciones cuando se abre la libreta de direcciones por primera vez. **SetDefaultDir** guarda el contenedor predeterminado como una entrada en el perfil. El contenedor permanece como predeterminado hasta que se realiza otra llamada a **SetDefaultDir** en la misma sesión o en otra sesión, o se quita el contenedor. 
  
> [!NOTE]
> La [PR_AB_CHOOSE_DIRECTORY_AUTOMATICALLY](pidtagaddressbookchoosedirectoryautomatically-canonical-property.md) propiedad corresponde a la opción Elegir **automáticamente** en el cuadro de diálogo Opciones de la libreta de direcciones. Cuando esta propiedad existe en la sección de perfil de [IID_CAPONE_PROF](https://msdn.microsoft.com/library/281aabc3-9656-299c-4c78-7733dc71050a%28Office.15%29.aspx) y se establece en **true**, el cuadro de diálogo libreta de direcciones ya no se establece de forma predeterminada en el contenedor especificado por **SetDefaultDir**, pero elige una libreta de direcciones que Microsoft Outlook considere apropiada para el contexto en el que se mostra el cuadro de diálogo. Tenga en cuenta que esto puede provocar una mala experiencia para proveedores de libretas de direcciones de terceros. 
  
## <a name="mfcmapi-reference"></a>Referencia de MFCMAPI

Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.
  
|**Archivo**|**Función**|**Comentario**|
|:-----|:-----|:-----|
|Abcontdlg.cpp  <br/> |CAbContDlg::OnSetDefaultDir  <br/> |MFCMAPI usa el **método SetDefaultDir** para convertir el contenedor de libreta de direcciones especificado en el predeterminado.  <br/> |
   
## <a name="see-also"></a>Consulte también



[IAddrBook::GetDefaultDir](iaddrbook-getdefaultdir.md)
  
[IAddrBook::GetSearchPath](iaddrbook-getsearchpath.md)
  
[IMAPISession::Logoff](imapisession-logoff.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IAddrBook : IMAPIProp](iaddrbookimapiprop.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

