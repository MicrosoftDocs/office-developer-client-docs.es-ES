---
title: Mantener una biblioteca de formularios
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8488f7ec-e44b-4d1a-ba42-baea8c71d350
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 6713055837e3b9b664d5fa1465c9a889919ee5ed
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590095"
---
# <a name="maintaining-a-form-library"></a><span data-ttu-id="369b6-103">Mantener una biblioteca de formularios</span><span class="sxs-lookup"><span data-stu-id="369b6-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="369b6-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="369b6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="369b6-105">Una biblioteca de formularios contiene toda la información importante acerca de un formulario: archivos ejecutables de su servidor, sus verbos y sus propiedades.</span><span class="sxs-lookup"><span data-stu-id="369b6-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="369b6-106">Algunos clientes de que sus usuarios puedan mantener, instalar o quitar servidores de formulario.</span><span class="sxs-lookup"><span data-stu-id="369b6-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="369b6-107">Si desea ofrecer esta característica a los usuarios, debe tener acceso a:</span><span class="sxs-lookup"><span data-stu-id="369b6-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="369b6-108">Archivo de configuración del servidor de formulario, un archivo con el. Extensión CFG.</span><span class="sxs-lookup"><span data-stu-id="369b6-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="369b6-109">Objeto de contenedor de la biblioteca de formularios, un objeto que implementa el [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) interfaz.</span><span class="sxs-lookup"><span data-stu-id="369b6-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="369b6-110">Para obtener acceso al archivo de configuración o una ruta de acceso a él, use cualquier medio es conveniente.</span><span class="sxs-lookup"><span data-stu-id="369b6-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="369b6-111">Normalmente, los clientes de presentan al usuario un cuadro de diálogo para la instalación y eliminación de servidores de formulario que también pueden utilizarse para solicitar al usuario de la ubicación del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="369b6-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="369b6-112">Para obtener acceso a contenedor de la biblioteca de formularios, llame al método [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) del director de formulario.</span><span class="sxs-lookup"><span data-stu-id="369b6-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="369b6-113">Pase un valor de enumeración para especificar qué biblioteca de formularios para abrir y si es necesario, un puntero al objeto que se debe usar el Administrador de formularios para abrir la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="369b6-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="369b6-114">Por ejemplo, si va a abrir una de [Las bibliotecas de formularios de carpeta](folder-form-libraries.md), pase una [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) puntero.</span><span class="sxs-lookup"><span data-stu-id="369b6-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="369b6-115">Una vez **OpenFormContainer** devuelve el puntero **IMAPIFormContainer** , llame a [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) o [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), según el mantenimiento que se debe realizar.</span><span class="sxs-lookup"><span data-stu-id="369b6-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="369b6-116">**InstallForm** agrega un servidor de formulario a la biblioteca; **RemoveForm** elimina un servidor de formulario de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="369b6-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

