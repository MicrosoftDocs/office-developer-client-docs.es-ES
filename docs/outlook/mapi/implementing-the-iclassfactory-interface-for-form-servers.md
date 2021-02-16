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
# <a name="implementing-the-iclassfactory-interface-for-form-servers"></a><span data-ttu-id="4c40e-103">Implementación de la interfaz IClassFactory para servidores de formulario</span><span class="sxs-lookup"><span data-stu-id="4c40e-103">Implementing the IClassFactory Interface for Form Servers</span></span>

  
  
<span data-ttu-id="4c40e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4c40e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4c40e-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) es la interfaz OLE que las aplicaciones cliente usan para crear nuevos objetos de formulario de la clase de mensaje del servidor de formulario.</span><span class="sxs-lookup"><span data-stu-id="4c40e-105">[IClassFactory](https://msdn.microsoft.com/library/ms694364%28VS.85%29.aspx) is the OLE interface that client applications use to create new form objects of your form server's message class.</span></span> <span data-ttu-id="4c40e-106">En la tabla siguiente se enumeran **los métodos IClassFactory** necesarios.</span><span class="sxs-lookup"><span data-stu-id="4c40e-106">The following table lists the **IClassFactory** methods that are required.</span></span> 
  
|<span data-ttu-id="4c40e-107">**Método**</span><span class="sxs-lookup"><span data-stu-id="4c40e-107">**Method**</span></span>|<span data-ttu-id="4c40e-108">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="4c40e-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4c40e-109">CreateInstance</span><span class="sxs-lookup"><span data-stu-id="4c40e-109">CreateInstance</span></span>](https://msdn.microsoft.com/library/ms682215%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="4c40e-110">Crea un nuevo objeto de formulario.</span><span class="sxs-lookup"><span data-stu-id="4c40e-110">Creates a new form object.</span></span>  <br/> |
|[<span data-ttu-id="4c40e-111">LockServer</span><span class="sxs-lookup"><span data-stu-id="4c40e-111">LockServer</span></span>](https://msdn.microsoft.com/library/ms682332%28v=VS.85%29.aspx) <br/> |<span data-ttu-id="4c40e-112">Bloquea el servidor de formularios en la memoria para que se pueda evitar la sobrecarga de inicio cuando se crean varios objetos de formulario.</span><span class="sxs-lookup"><span data-stu-id="4c40e-112">Locks the form server in memory so that startup overhead can be avoided when multiple form objects are created.</span></span>  <br/> |
   
<span data-ttu-id="4c40e-113">Para obtener toda la información necesaria para implementar estos métodos, consulta la sección COM y ActiveX Object Services en Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="4c40e-113">For all the information necessary to implement these methods, see the COM and ActiveX Object Services section in the Windows SDK.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4c40e-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="4c40e-114">See also</span></span>



[<span data-ttu-id="4c40e-115">Escritura de código de servidor de formulario</span><span class="sxs-lookup"><span data-stu-id="4c40e-115">Writing Form Server Code</span></span>](writing-form-server-code.md)

