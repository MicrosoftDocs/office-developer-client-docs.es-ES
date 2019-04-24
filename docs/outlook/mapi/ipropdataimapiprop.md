---
title: IPropData IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData
api_type:
- COM
ms.assetid: 30b8ae9e-0c0c-4468-b286-29e083696fed
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: aed9120ac264a6c47c9d02502093e56d3268d08a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279545"
---
# <a name="ipropdata--imapiprop"></a>IPropData : IMAPIProp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Proporciona la capacidad de recuperar y cambiar el acceso de las propiedades de un objeto. 
  
|||
|:-----|:-----|
|Archivo de encabezado:  <br/> |Mapiutil. h  <br/> |
|Expuesto por:  <br/> |Objeto de datos de propiedad  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Llamado por:  <br/> |Proveedores de servicios y aplicaciones de cliente  <br/> |
|Identificador de interfaz:  <br/> |IID_IMAPIPropData  <br/> |
|Tipo de puntero:  <br/> |LPPROPDATA  <br/> |
|Modelo de transacción:  <br/> |No transactd  <br/> |
   
## <a name="vtable-order"></a>Orden vtable

|||
|:-----|:-----|
|[HrSetObjAccess](ipropdata-hrsetobjaccess.md) <br/> |Establece el nivel de acceso para el objeto.  <br/> |
|[HrSetPropAccess](ipropdata-hrsetpropaccess.md) <br/> |Establece el nivel de acceso y el estado de una o varias de las propiedades del objeto.  <br/> |
|[HrGetPropAccess](ipropdata-hrgetpropaccess.md) <br/> |Recupera el nivel de acceso y el estado de una o varias de las propiedades del objeto.  <br/> |
|[HrAddObjProps](ipropdata-hraddobjprops.md) <br/> |Agrega una o más propiedades de tipo PT Object al objeto.  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI implementa la interfaz **IPropData:: IMAPIProp** y la usan principalmente los proveedores de servicios que tienen acceso a esta implementación mediante una llamada a la función [CreateIProp](createiprop.md) . 
  
Para obtener más información acerca de los niveles de acceso en objetos y propiedades, consulte [permisos para objetos y propiedades](permissions-for-mapi-objects-and-properties.md).
  
## <a name="see-also"></a>Vea también



[Interfaces MAPI](mapi-interfaces.md)

