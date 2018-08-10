---
title: MAPIERROR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.MAPIERROR
api_type:
- COM
ms.assetid: e04c2228-aa0a-4958-b5b2-6467e93ab613
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d0ddff638e26940ea74932a8a491455f67cc8dd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818243"
---
# <a name="mapierror"></a><span data-ttu-id="0a120-103">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="0a120-103">MAPIERROR</span></span>

  
  
<span data-ttu-id="0a120-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0a120-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0a120-105">Proporciona información detallada sobre un error, normalmente generado por el sistema operativo, MAPI o un proveedor de servicios.</span><span class="sxs-lookup"><span data-stu-id="0a120-105">Provides detailed information about an error, typically generated by the operating system, MAPI, or a service provider.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0a120-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="0a120-106">Header file:</span></span>  <br/> |<span data-ttu-id="0a120-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0a120-107">Mapidefs.h</span></span>  <br/> |
   
```cpp
typedef struct _MAPIERROR
{
  ULONG ulVersion;
  LPSTR lpszError;
  LPSTR lpszComponent;
  ULONG ulLowLevelError;
  ULONG ulContext;
} MAPIERROR, FAR * LPMAPIERROR;

```

## <a name="members"></a><span data-ttu-id="0a120-108">Members</span><span class="sxs-lookup"><span data-stu-id="0a120-108">Members</span></span>

 <span data-ttu-id="0a120-109">**ulVersion**</span><span class="sxs-lookup"><span data-stu-id="0a120-109">**ulVersion**</span></span>
  
> <span data-ttu-id="0a120-110">Número de versión de la estructura.</span><span class="sxs-lookup"><span data-stu-id="0a120-110">Version number of the structure.</span></span> <span data-ttu-id="0a120-111">El miembro **ulVersion** se usa para la expansión futura y debe establecerse en MAPI_ERROR_VERSION, que actualmente se define como cero.</span><span class="sxs-lookup"><span data-stu-id="0a120-111">The **ulVersion** member is used for future expansion and should be set to MAPI_ERROR_VERSION, which is currently defined as zero.</span></span> 
    
 <span data-ttu-id="0a120-112">**lpszError**</span><span class="sxs-lookup"><span data-stu-id="0a120-112">**lpszError**</span></span>
  
> <span data-ttu-id="0a120-113">Puntero a una cadena que describe el error.</span><span class="sxs-lookup"><span data-stu-id="0a120-113">Pointer to a string that describes the error.</span></span> <span data-ttu-id="0a120-114">Esta cadena estará en formato Unicode si se establece el parámetro _ulFlags_ al método en el que se usa esta estructura en MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="0a120-114">This string will be in Unicode format if the  _ulFlags_ parameter to the method in which this structure is used is set to MAPI_UNICODE.</span></span> 
    
 <span data-ttu-id="0a120-115">**lpszComponent**</span><span class="sxs-lookup"><span data-stu-id="0a120-115">**lpszComponent**</span></span>
  
> <span data-ttu-id="0a120-116">Puntero a una cadena que describe el componente que generó el error.</span><span class="sxs-lookup"><span data-stu-id="0a120-116">Pointer to a string that describes the component that generated the error.</span></span> <span data-ttu-id="0a120-117">Esta cadena estará en formato Unicode si se establece el parámetro _ulFlags_ al método en el que se usa esta estructura en MAPI_UNICODE..</span><span class="sxs-lookup"><span data-stu-id="0a120-117">This string will be in Unicode format if the  _ulFlags_ parameter to the method in which this structure is used is set to MAPI_UNICODE.</span></span> 
    
 <span data-ttu-id="0a120-118">**ulLowLevelError**</span><span class="sxs-lookup"><span data-stu-id="0a120-118">**ulLowLevelError**</span></span>
  
> <span data-ttu-id="0a120-119">Valor de error de bajo nivel que se usa sólo cuando el error que se devuelve es bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="0a120-119">Low-level error value that is used only when the error to be returned is low-level.</span></span>
    
 <span data-ttu-id="0a120-120">**ulContext**</span><span class="sxs-lookup"><span data-stu-id="0a120-120">**ulContext**</span></span>
  
> <span data-ttu-id="0a120-121">Valor que representa la ubicación en el componente que señala el miembro **lpszComponent** que identifica donde se produjo el error.</span><span class="sxs-lookup"><span data-stu-id="0a120-121">Value that represents the location in the component pointed to by the **lpszComponent** member that identifies where the error occurred.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0a120-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="0a120-122">Remarks</span></span>

<span data-ttu-id="0a120-123">La estructura **MAPIERROR** se usa para describir la información de error.</span><span class="sxs-lookup"><span data-stu-id="0a120-123">The **MAPIERROR** structure is used to describe error information.</span></span> <span data-ttu-id="0a120-124">Los clientes y proveedores de servicios de pasan un puntero a una estructura **MAPIERROR** en el parámetro _lppMAPIError_ del método [IMAPIProp::GetLastError](imapiprop-getlasterror.md) .</span><span class="sxs-lookup"><span data-stu-id="0a120-124">Clients and service providers pass a pointer to a **MAPIERROR** structure in the  _lppMAPIError_ parameter of the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> <span data-ttu-id="0a120-125">**GetLastError** devuelve información sobre el error anterior que se ha producido a un objeto.</span><span class="sxs-lookup"><span data-stu-id="0a120-125">**GetLastError** returns information about the previous error that has occurred to an object.</span></span> <span data-ttu-id="0a120-126">Los autores de llamadas de **GetLastError** libere la memoria para la estructura **MAPIERROR** mediante una llamada [MAPIFreeBuffer](mapifreebuffer.md).</span><span class="sxs-lookup"><span data-stu-id="0a120-126">Callers of **GetLastError** free the memory for the **MAPIERROR** structure by calling [MAPIFreeBuffer](mapifreebuffer.md).</span></span>
  
<span data-ttu-id="0a120-127">El miembro **lpszComponent** puede utilizarse para asignar el archivo de Ayuda del componente, si lo hay.</span><span class="sxs-lookup"><span data-stu-id="0a120-127">The **lpszComponent** member can be used to map the component's Help file, if one exists.</span></span> <span data-ttu-id="0a120-128">Proveedores de servicios deben limitar el tamaño de la cadena de componente a 30 caracteres para que se puede mostrar fácilmente en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="0a120-128">Service providers should limit the size of the component string to 30 characters so that it can easily be displayed in a dialog box.</span></span> <span data-ttu-id="0a120-129">El miembro **ulContext** también puede usarse para hacer referencia a un tema de ayuda en pantalla de los errores comunes.</span><span class="sxs-lookup"><span data-stu-id="0a120-129">The **ulContext** member can also be used to refer to an online Help topic for common errors.</span></span> 
  
<span data-ttu-id="0a120-130">Debido a que los proveedores de servicio no son necesarios para proporcionar información detallada del error, los clientes no deben esperar que cualquiera de los miembros de la estructura **MAPIERROR** que se devuelven para contener datos válidos.</span><span class="sxs-lookup"><span data-stu-id="0a120-130">Because service providers are not required to provide detailed error information, clients should not expect any of the members of the **MAPIERROR** structure that are returned to contain valid data.</span></span> <span data-ttu-id="0a120-131">Sin embargo, en un mínimo MAPI recomienda encarecidamente que los proveedores de especifican información en los miembros **lpszComponent** y **ulContext** .</span><span class="sxs-lookup"><span data-stu-id="0a120-131">However, at a minimum MAPI strongly recommends that providers specify information in the **lpszComponent** and **ulContext** members.</span></span> 
  
<span data-ttu-id="0a120-132">Para obtener más información acerca de control de errores en MAPI, vea [Control de errores](error-handling-in-mapi.md).</span><span class="sxs-lookup"><span data-stu-id="0a120-132">For more information about error handling in MAPI, see [Error Handling](error-handling-in-mapi.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0a120-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="0a120-133">See also</span></span>



[<span data-ttu-id="0a120-134">IABLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-134">IABLogon::GetLastError</span></span>](iablogon-getlasterror.md)
  
[<span data-ttu-id="0a120-135">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="0a120-135">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="0a120-136">IMAPIControl::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-136">IMAPIControl::GetLastError</span></span>](imapicontrol-getlasterror.md)
  
[<span data-ttu-id="0a120-137">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-137">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="0a120-138">IMAPISession::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-138">IMAPISession::GetLastError</span></span>](imapisession-getlasterror.md)
  
[<span data-ttu-id="0a120-139">IMAPISupport::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-139">IMAPISupport::GetLastError</span></span>](imapisupport-getlasterror.md)
  
[<span data-ttu-id="0a120-140">IMAPISupport::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="0a120-140">IMAPISupport::OpenAddressBook</span></span>](imapisupport-openaddressbook.md)
  
[<span data-ttu-id="0a120-141">IMAPISession::OpenAddressBook</span><span class="sxs-lookup"><span data-stu-id="0a120-141">IMAPISession::OpenAddressBook</span></span>](imapisession-openaddressbook.md)
  
[<span data-ttu-id="0a120-142">IMAPITable::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-142">IMAPITable::GetLastError</span></span>](imapitable-getlasterror.md)
  
[<span data-ttu-id="0a120-143">IMsgServiceAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-143">IMsgServiceAdmin::GetLastError</span></span>](imsgserviceadmin-getlasterror.md)
  
[<span data-ttu-id="0a120-144">IMSLogon::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-144">IMSLogon::GetLastError</span></span>](imslogon-getlasterror.md)
  
[<span data-ttu-id="0a120-145">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="0a120-145">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="0a120-146">IProfAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-146">IProfAdmin::GetLastError</span></span>](iprofadmin-getlasterror.md)
  
[<span data-ttu-id="0a120-147">IProviderAdmin::GetLastError</span><span class="sxs-lookup"><span data-stu-id="0a120-147">IProviderAdmin::GetLastError</span></span>](iprovideradmin-getlasterror.md)


[<span data-ttu-id="0a120-148">Estructuras MAPI</span><span class="sxs-lookup"><span data-stu-id="0a120-148">MAPI Structures</span></span>](mapi-structures.md)
