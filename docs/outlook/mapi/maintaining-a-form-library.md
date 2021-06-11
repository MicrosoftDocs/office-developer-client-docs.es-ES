---
title: Mantenimiento de una biblioteca de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 51c7c3f8ba70dcb3d35dc50806e984fd4b193818
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408806"
---
# <a name="maintaining-a-form-library"></a>Mantenimiento de una biblioteca de formularios

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una biblioteca de formularios contiene toda la información importante sobre un formulario: sus propiedades, sus verbos y los archivos ejecutables de su servidor. Algunos clientes permiten a sus usuarios mantener, instalar o quitar servidores de formulario. Si desea ofrecer esta característica a los usuarios, debe tener acceso a:
  
- El archivo de configuración del servidor de formularios, un archivo con el archivo . Extensión CFG.
    
- Objeto contenedor de la biblioteca de formularios, un objeto que implementa la [interfaz IMAPIFormContainer : IUnknown.](imapiformcontaineriunknown.md) 
    
Para obtener acceso al archivo de configuración o a un nombre de ruta de acceso, use los medios que sean convenientes. Normalmente, los clientes presentan al usuario un cuadro de diálogo para instalar y quitar servidores de formulario que también se pueden usar para solicitar al usuario la ubicación del archivo de configuración.
  
Para obtener acceso al contenedor de la biblioteca de formularios, llame al método [IMAPIFormMgr::OpenFormContainer del](imapiformmgr-openformcontainer.md) administrador de formularios. Pase un valor de enumeración para especificar la biblioteca de formularios que se va a abrir y, si es necesario, un puntero al objeto que el administrador de formularios debe usar para abrir la biblioteca de formularios. Por ejemplo, si va a abrir una carpeta [Bibliotecas de formularios](folder-form-libraries.md), pase un [puntero IMAPIFolder : IMAPIContainer.](imapifolderimapicontainer.md) 
  
Después **de que OpenFormContainer** devuelva el puntero **IMAPIFormContainer,** llame a [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) o [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), en función del mantenimiento que se va a realizar. **InstallForm** agrega un servidor de formulario a la biblioteca; **RemoveForm** elimina un servidor de formulario de la biblioteca. 
  

