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
# <a name="maintaining-a-form-library"></a><span data-ttu-id="a4c9e-103">Mantenimiento de una biblioteca de formularios</span><span class="sxs-lookup"><span data-stu-id="a4c9e-103">Maintaining a Form Library</span></span>

  
  
<span data-ttu-id="a4c9e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a4c9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a4c9e-105">Una biblioteca de formularios contiene toda la información importante sobre un formulario: sus propiedades, sus verbos y los archivos ejecutables del servidor.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-105">A form library holds all of the important information about a form: its properties, its verbs, and its server's executable files.</span></span> <span data-ttu-id="a4c9e-106">Algunos clientes permiten a los usuarios mantener, instalar o quitar servidores de formularios.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-106">Some clients allow their users to maintain, install, or remove form servers.</span></span> <span data-ttu-id="a4c9e-107">Si desea ofrecer esta característica a los usuarios, debe tener acceso a:</span><span class="sxs-lookup"><span data-stu-id="a4c9e-107">If you want to offer this feature to your users, you must have access to:</span></span>
  
- <span data-ttu-id="a4c9e-108">El archivo de configuración del servidor de formularios, un archivo con el. CFG.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-108">The form server's configuration file, a file with the .CFG extension.</span></span>
    
- <span data-ttu-id="a4c9e-109">Objeto Container de la biblioteca de formularios, un objeto que implementa la interfaz [IMAPIFormContainer: IUnknown](imapiformcontaineriunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c9e-109">The form library's container object, an object that implements the [IMAPIFormContainer : IUnknown](imapiformcontaineriunknown.md) interface.</span></span> 
    
<span data-ttu-id="a4c9e-110">Para tener acceso al archivo de configuración o a un directorio, use los medios que sean convenientes.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-110">To access the configuration file or a pathname to it, use whatever means are convenient.</span></span> <span data-ttu-id="a4c9e-111">Normalmente, los clientes presentan al usuario un cuadro de diálogo para instalar y quitar servidores de formularios que también se pueden usar para solicitar al usuario la ubicación del archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-111">Usually, clients present the user with a dialog box for installing and removing form servers that can also be used to prompt the user for the location of the configuration file.</span></span>
  
<span data-ttu-id="a4c9e-112">Para tener acceso al contenedor de la biblioteca de formularios, llame al método [IMAPIFormMgr:: OpenFormContainer](imapiformmgr-openformcontainer.md) del administrador de formularios.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-112">To access the form library's container, call the form manager's [IMAPIFormMgr::OpenFormContainer](imapiformmgr-openformcontainer.md) method.</span></span> <span data-ttu-id="a4c9e-113">Pase un valor de enumeración para especificar la biblioteca de formularios que se va a abrir y, si es necesario, un puntero al objeto que debe usar el administrador de formularios para abrir la biblioteca de formularios.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-113">Pass in an enumeration value to specify which form library to open, and if necessary, a pointer to the object that the form manager should use to open the form library.</span></span> <span data-ttu-id="a4c9e-114">Por ejemplo, si abre una biblioteca de [formularios de carpetas](folder-form-libraries.md), pase un puntero [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="a4c9e-114">For example, if you are opening a [Folder Form Libraries](folder-form-libraries.md), pass an [IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md) pointer.</span></span> 
  
<span data-ttu-id="a4c9e-115">Una vez que **OpenFormContainer** devuelve el puntero **IMAPIFormContainer** , llame a [IMAPIFormContainer:: InstallForm](imapiformcontainer-installform.md) o [IMAPIFormContainer:: RemoveForm](imapiformcontainer-removeform.md), según el mantenimiento que se vaya a realizar.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-115">After **OpenFormContainer** returns the **IMAPIFormContainer** pointer, call either [IMAPIFormContainer::InstallForm](imapiformcontainer-installform.md) or [IMAPIFormContainer::RemoveForm](imapiformcontainer-removeform.md), depending on the maintenance to be performed.</span></span> <span data-ttu-id="a4c9e-116">**InstallForm** agrega un servidor de formularios a la biblioteca; **RemoveForm** elimina un servidor de formularios de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a4c9e-116">**InstallForm** adds a form server to the library; **RemoveForm** deletes a form server from the library.</span></span> 
  

