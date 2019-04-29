---
title: Copiar o mover un mensaje o una carpeta
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Última modificación: 8 de noviembre de 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413503"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="ad8c5-103">Copiar o mover un mensaje o una carpeta</span><span class="sxs-lookup"><span data-stu-id="ad8c5-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="ad8c5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad8c5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad8c5-105">Un cliente puede usar uno de cuatro métodos para copiar o mover un mensaje o una carpeta:</span><span class="sxs-lookup"><span data-stu-id="ad8c5-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="ad8c5-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="ad8c5-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="ad8c5-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="ad8c5-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="ad8c5-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="ad8c5-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="ad8c5-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="ad8c5-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="ad8c5-110">Al establecer los indicadores y los parámetros apropiados \*\*\*\* , se puede realizar CopyTo y **CopyProps** para que funcione igual que **CopyFolder** o **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="ad8c5-111">Tenga en cuenta los siguientes aspectos a la hora de decidir qué método llamar:</span><span class="sxs-lookup"><span data-stu-id="ad8c5-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="ad8c5-112">¿Está copiando o moviendo una carpeta o un mensaje?</span><span class="sxs-lookup"><span data-stu-id="ad8c5-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="ad8c5-113">¿Cuánto sabe sobre la carpeta o el mensaje que se va a mover o copiar?</span><span class="sxs-lookup"><span data-stu-id="ad8c5-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="ad8c5-114">¿Cuántas de las propiedades de la carpeta o del mensaje se moverán o se copiarán?</span><span class="sxs-lookup"><span data-stu-id="ad8c5-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="ad8c5-115">Puede usar los métodos **IMAPIProp** para copiar o mover una carpeta o un mensaje.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="ad8c5-116">**IMAPIFolder:: CopyMessages** solo funciona con mensajes; **IMAPIFolder:: CopyFolder** solo funciona con carpetas.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="ad8c5-117">Mientras que el uso de los métodos **IMAPIFolder** no requiere ningún conocimiento de las propiedades que admite la carpeta o el mensaje que se va a copiar o mover, debe tener algunos conocimientos para usar los métodos **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="ad8c5-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="ad8c5-118">Con **IMAPIProp:: CopyProps**, debe poder especificar explícitamente cuál de las propiedades de la carpeta o del mensaje desea copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="ad8c5-119">Con **IMAPIProp:: CopyTo**, a menos que desee copiar o mover todas las propiedades, debe especificar explícitamente cuáles se deben excluir.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="ad8c5-120">Para obtener más información acerca de estos métodos, consulte [copia de propiedades MAPI](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ad8c5-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="ad8c5-121">El número de propiedades que se va a copiar o mover puede afectar a la decisión sobre el método que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="ad8c5-122">Si va a copiar o mover varios mensajes, llame a **IMAPIFolder:: CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="ad8c5-123">Una opción alternativa es llamar a **IMAPIProp:: CopyProps** para copiar solo la propiedad **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) de la carpeta.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="ad8c5-124">El siguiente procedimiento muestra cómo usar **CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="ad8c5-125">Para copiar o mover uno o más mensajes</span><span class="sxs-lookup"><span data-stu-id="ad8c5-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="ad8c5-126">Busque identificadores de entrada válidos para las carpetas de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="ad8c5-127">Para abrir estas carpetas en modo de lectura y escritura, llame a [IMAPISession:: OpenEntry](imapisession-openentry.md) o [IMsgStore:: OpenEntry](imsgstore-openentry.md) y establezca la marca MAPI_MODIFY.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="ad8c5-128">Compruebe que el puntero de interfaz devuelto desde **OpenEntry** es un puntero de interfaz **IMAPIFolder** .</span><span class="sxs-lookup"><span data-stu-id="ad8c5-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="ad8c5-129">Si no es así, conviértala al tipo LPMAPIFOLDER.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="ad8c5-130">Cree una matriz de identificadores de entrada que representen uno o más mensajes que se van a copiar o mover.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="ad8c5-131">Llame a **IMAPIFolder:: CopyMessages** con los siguientes indicadores establecidos:</span><span class="sxs-lookup"><span data-stu-id="ad8c5-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="ad8c5-132">MESSAGE_MOVE, si desea realizar una operación de movimiento.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="ad8c5-133">MESSAGE_DIALOG y pase un identificador de ventana en el parámetro _ulUIParam_ si desea que la carpeta muestre un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="ad8c5-134">Libere los punteros **IMAPIFolder** para las carpetas de origen y de destino.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="ad8c5-135">Si desea copiar el contenido completo de una carpeta a otra carpeta, llame al método **IMAPIFolder:: CopyFolder** o **IMAPIProp:: CopyTo** de la carpeta de origen.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="ad8c5-136">Para copiar algunas de las propiedades de una carpeta, llame a su método **IMAPIProp:: CopyProps** .</span><span class="sxs-lookup"><span data-stu-id="ad8c5-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="ad8c5-137">Para copiar la mayoría de las propiedades de una carpeta, llame a **IMAPIProp:: CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="ad8c5-138">Por ejemplo, si quiere copiar las propiedades **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) y **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) de una carpeta, tiene las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="ad8c5-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="ad8c5-139">Llame a **IMAPIFolder:: CopyFolder** para copiar todas las propiedades de la carpeta y, a continuación, elimine las no deseadas de la nueva carpeta.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="ad8c5-140">Llame \*\*\*\* a CopyTo y excluya todas las propiedades de la carpeta excepto **PR_DISPLAY_NAME** y **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="ad8c5-141">Llame a **CopyProps**, pasando **PR_DISPLAY_NAME** y **PR_COMMENT** en la matriz include.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="ad8c5-142">En este caso, **CopyProps** es la mejor opción porque está pensada para ser utilizada para copiar un pequeño conjunto de propiedades y es la llamada más fácil de implementar.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="ad8c5-143">Para copiar o mover sólo las propiedades de la carpeta, sin incluir los mensajes, llame al método **IMAPIProp:: CopyTo** de la carpeta y excluya las siguientes propiedades:</span><span class="sxs-lookup"><span data-stu-id="ad8c5-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="ad8c5-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad8c5-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="ad8c5-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="ad8c5-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="ad8c5-146">Los métodos Copy pueden devolver S_OK, que indican que el resultado es correcto, MAPI_W_PARTIAL_COMPLETION, que indica que se ha realizado parcialmente correctamente o un error.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="ad8c5-147">Si se devuelve MAPI_W_PARTIAL_COMPLETION, use la macro **HR_FAILED** para obtener acceso a un error más específico.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="ad8c5-148">Para obtener más información, consulte [usar macros para el control de errores](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="ad8c5-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="ad8c5-149">Si copia mensajes de un almacén de mensajes en otro y Unicode no es compatible con ambas, tenga en cuenta que la información se puede perder debido a la conversión de la página de códigos.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="ad8c5-150">Por lo general, no se puede saber si los almacenes de mensajes admiten uno o ambos formatos, lo que impide determinar si se copian las propiedades de texto como cadenas ASCII o como cadenas Unicode.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="ad8c5-151">Si admite Unicode, intente realizar una copia Unicode; Si se produce un error con el valor de error MAPI_E_BAD_CHARWIDTH, se recurre a ASCII.</span><span class="sxs-lookup"><span data-stu-id="ad8c5-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

