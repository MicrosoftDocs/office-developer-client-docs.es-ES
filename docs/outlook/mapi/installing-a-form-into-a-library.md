---
title: Instalación de un formulario en una biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 54b2dece31937b1ff233d4d1e7d8bbc198bfe118
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817836"
---
# <a name="installing-a-form-into-a-library"></a>Instalación de un formulario en una biblioteca

  
  
**Se aplica a**: Outlook 
  
El Administrador de formularios MAPI predeterminada que se proporciona con el SDK de Windows no proporciona una interfaz de usuario para la instalación de formularios en las diversas bibliotecas de formulario. Por este motivo, debe crear una aplicación pequeña: o detallada conjunto de instrucciones, que los usuarios pueden usar para instalar el formulario.
  
Si implementa una aplicación de instalación, la serie de acciones que debe realizar para instalar un formulario en contenido asociada de una carpeta tabla son los siguientes:
  
1. Llame a la función [MAPIOpenFormMgr](mapiopenformmgr.md) para abrir el formulario de administrador. 
    
2. Utilice el método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) o [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para seleccionar y abrir el contenedor de destino para el formulario. 
    
3. Use la función [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar el formulario. 
    
    Son los pasos del 4 al 6 para su instalación en una biblioteca de formularios local:
    
4. Copie todos los archivos en el lugar adecuado en el disco local, si la instalación es para la biblioteca de formularios local en la estación de trabajo del usuario. Si es necesario, modifique el archivo de configuración de formulario para reflejar las rutas de acceso actuales de los componentes. El archivo de configuración de formulario puede contener rutas de acceso relativas, en cuyo caso este paso puede no ser necesario.
    
5. Complete los pasos de registro OLE apropiados para asociar el tipo de mensaje con el servidor de formulario que se va a instalar.
    
6. Si el formulario se ha instalado en la biblioteca de formularios local, copie el formulario icono (.ico) y los archivos de configuración (.cfg) en el directorio %WINDOWS%\FORMS\CONFIGS por lo que el formulario se puede restaurar automáticamente en caso de que la biblioteca de formularios se daña o se elimina. Este paso es recomendable pero no obligatorio.
    
> [!NOTE]
> Puede simplificar la instalación a una biblioteca de formularios local mediante el reemplazo de los pasos 1 y 2 con una llamada a la función [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . 
  
## <a name="see-also"></a>Ver también



[Desarrollo de los servidores de formulario MAPI](developing-mapi-form-servers.md)

