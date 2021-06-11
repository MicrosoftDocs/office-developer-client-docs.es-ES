---
title: Instalación de un formulario en una biblioteca
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 303c9dcb-f9b5-4cea-b5f2-3eba01aa3b09
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 08470a80153e42136922ae502252d83de0125512
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433146"
---
# <a name="installing-a-form-into-a-library"></a>Instalación de un formulario en una biblioteca

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
El administrador de formularios MAPI predeterminado proporcionado con el SDK de Windows no proporciona una interfaz de usuario para instalar formularios en las distintas bibliotecas de formularios. Debido a esto, tendrá que crear una aplicación pequeña (o un conjunto detallado de instrucciones) que los usuarios puedan usar para instalar el formulario.
  
Si implementa una aplicación de instalación, la serie de acciones que debe realizar para instalar un formulario en la tabla de contenido asociada de una carpeta son las siguientes:
  
1. Llame a [la función MAPIOpenFormMgr](mapiopenformmgr.md) para abrir el administrador de formularios. 
    
2. Use [el método IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) o [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) para seleccionar y abrir el contenedor de destino del formulario. 
    
3. Use la [función IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) para instalar el formulario. 
    
    Los pasos del 4 al 6 son para la instalación en una biblioteca de formularios local:
    
4. Copie todos los archivos en el lugar adecuado en el disco local, si la instalación es en la biblioteca de formularios local de la estación de trabajo del usuario. Si es necesario, modifique el archivo de configuración del formulario para reflejar las rutas de acceso actuales de los componentes. El archivo de configuración del formulario puede contener rutas de acceso relativas, en cuyo caso este paso puede no ser necesario.
    
5. Complete los pasos de registro OLE adecuados para asociar el tipo de mensaje con el servidor de formulario que se va a instalar.
    
6. Si el formulario se instaló en la biblioteca de formularios local, copie el icono del formulario (.ico) y los archivos de configuración (.cfg) en el directorio %WINDOWS%\FORMS\CONFIGS para que el formulario se pueda restaurar automáticamente en caso de que la biblioteca de formularios esté dañada o eliminada. Este paso se recomienda, pero no es obligatorio.
    
> [!NOTE]
> Puede simplificar la instalación en una biblioteca de formularios local reemplazando los pasos 1 y 2 por una llamada a la [función MAPIOpenLocalFormContainer.](mapiopenlocalformcontainer.md) 
  
## <a name="see-also"></a>Vea también



[Desarrollo de servidores de formulario MAPI](developing-mapi-form-servers.md)

