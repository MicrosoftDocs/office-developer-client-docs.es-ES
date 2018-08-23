---
title: IProfAdminGetProfileTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IProfAdmin.GetProfileTable
api_type:
- COM
ms.assetid: cebccd2d-8215-486e-9964-7fc42412cec6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8b1b037cf24c1bb5a0c84da3d59892ab15763f37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588247"
---
# <a name="iprofadmingetprofiletable"></a>IProfAdmin::GetProfileTable

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona acceso a la tabla de perfil, una tabla que contiene información acerca de todos los perfiles disponibles.
  
```cpp
HRESULT GetProfileTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [entrada] Siempre es NULL.
    
 _lppTable_
  
> [out] Un puntero a un puntero a la tabla de perfil.
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La tabla de perfil se recuperó correctamente.
    
## <a name="remarks"></a>Comentarios

El método **IProfAdmin::GetProfileTable** proporciona acceso a la tabla de perfil, que contiene una fila por cada perfil disponible. Hay sólo dos columnas de cada fila: nombre para mostrar del perfil y una marca que indica si el perfil es el valor predeterminado. 
  
Los perfiles que se han eliminado, o que están en uso pero que se han marcado para su eliminación, no se incluyen en la tabla de perfil. La tabla de perfil es estática; subsiguientes adiciones y eliminaciones de perfiles no se reflejan en la tabla. 
  
Si no hay perfiles existen, **GetProfileTable** devuelve un objeto table con cero filas. 
  
Para obtener más información acerca de la tabla de perfil, vea [Las tablas de perfil](profile-tables.md). 
  
## <a name="mfcmapi-reference"></a>Referencia MFCMAPI

MFCMAPI c�digo de ejemplo, vea la siguiente tabla.
  
|**Archivo**|**Funci�n**|**Comentario**|
|:-----|:-----|:-----|
|MainDlg.cpp  <br/> |CMainDlg::OnShowProfiles  <br/> |MFCMAPI usa el método **IProfAdmin::GetProfileTable** para obtener la tabla de perfil para mostrar un cuadro de diálogo nuevo.  <br/> |
   
## <a name="see-also"></a>Recursos adicionales



[IMAPITable : IUnknown](imapitableiunknown.md)
  
[MAPILogonEx](mapilogonex.md)
  
[IProfAdmin : IUnknown](iprofadminiunknown.md)


[MFCMAPI como un ejemplo de c�digo](mfcmapi-as-a-code-sample.md)

