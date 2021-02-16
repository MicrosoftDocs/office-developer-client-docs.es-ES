---
title: Implementación de la interfaz IClassFactory para servidores de formulario
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22402261-c0fc-49bd-a222-e31989d6ff30
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 12d854b72632653d9e1081c9e726c0fe7087bc27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310034"
---
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a>Implementación de la interfaz IClassFactory para servidores de formulario

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) es la interfaz OLE que las aplicaciones cliente usan para crear nuevos objetos de formulario de la clase de mensaje del servidor de formulario. En la tabla siguiente se enumeran **los métodos IClassFactory** necesarios. 
  
|**Método**|**Descripción**|
|:-----|:-----|
|[CreateInstance](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |Crea un nuevo objeto de formulario.  <br/> |
|[LockServer](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |Bloquea el servidor de formularios en la memoria para que se pueda evitar la sobrecarga de inicio cuando se crean varios objetos de formulario.  <br/> |
   
Para obtener toda la información necesaria para implementar estos métodos, consulta la sección COM y ActiveX Object Services en Windows SDK.
  
## <a name="see-also"></a>Consulte también



[Escritura de código de servidor de formulario](writing-form-server-code.md)

