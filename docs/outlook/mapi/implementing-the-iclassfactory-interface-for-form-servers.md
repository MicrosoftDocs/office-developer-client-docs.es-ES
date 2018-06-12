---
title: Implementación de la interfaz IClassFactory para los servidores de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 3ecae23d8631c818fb3d1c6786b2d180e9f32a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817706"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementación de la interfaz IClassFactory para los servidores de formulario

  
  
**Se aplica a**: Outlook 
  
[IClassFactory](http://msdn.microsoft.com/en-us/library/ms694364%28VS.85%29.aspx) es la interfaz OLE que las aplicaciones cliente que se usan para crear nuevos objetos de formulario de clase de mensaje del servidor de su formulario. En la siguiente tabla se enumera los métodos de **IClassFactory** que son necesarios. 
  
|**Método**|**Descripción**|
|:-----|:-----|
|[CreateInstance](http://msdn.microsoft.com/en-us/library/ms682215%28v=VS.85%29.aspx) <br/> |Crea un nuevo objeto de formulario.  <br/> |
|[LockServer](http://msdn.microsoft.com/en-us/library/ms682332%28v=VS.85%29.aspx) <br/> |Bloquea el servidor de formulario en la memoria para que se puede evitar la sobrecarga de inicio cuando se crean varios objetos de formulario.  <br/> |
   
Para toda la información necesaria para implementar estos métodos, vea la sección Servicios de objeto de ActiveX y COM en el SDK de Windows.
  
## <a name="see-also"></a>Ver también



[Escritura de código de servidor de formulario](writing-form-server-code.md)

