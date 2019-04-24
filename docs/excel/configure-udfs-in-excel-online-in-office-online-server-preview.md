---
title: Configurar las UDF en Excel online en Office Online Server
manager: soliver
ms.date: 03/18/2016
ms.audience: ITPro
localization_priority: Normal
ms.assetid: 3e0ca274-e9cd-48a1-8cfc-9d5053738972
description: Use funciones definidas por el usuario (UDF) en Excel online en Office Online Server para llamar a funciones personalizadas.
ms.openlocfilehash: dbba60a62a1a4783b47c3f1fe40a118dd8ed0d6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311063"
---
# <a name="configure-udfs-in-excel-online-in-office-online-server"></a><span data-ttu-id="c6d5e-103">Configurar las UDF en Excel online en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="c6d5e-103">Configure UDFs in Excel Online in Office Online Server</span></span>

<span data-ttu-id="c6d5e-104">Use funciones definidas por el usuario (UDF) en Excel online en Office Online Server para llamar a funciones personalizadas.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-104">Use user-defined functions (UDFs) in Excel Online in Office Online Server to call custom functions.</span></span> 
  
<span data-ttu-id="c6d5e-105">Las funciones definidas por el usuario (UDF) en Excel online permiten llamar a funciones personalizadas escritas en código administrado mediante fórmulas en las celdas.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-105">User-defined functions (UDFs) in Excel Online enable you to call custom functions written in managed code by using formulas in cells.</span></span> <span data-ttu-id="c6d5e-106">Puede usar las UDF para:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-106">You can use UDFs to:</span></span>
  
- <span data-ttu-id="c6d5e-107">Call custom mathematical functions.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-107">Call custom mathematical functions.</span></span>
    
- <span data-ttu-id="c6d5e-108">Get data from custom data sources into worksheets.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-108">Get data from custom data sources into worksheets.</span></span>
    
- <span data-ttu-id="c6d5e-109">Llamar a servicios Web.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-109">Call web services.</span></span>
    
<span data-ttu-id="c6d5e-110">Puede instalar archivos binarios de UDF en una de estas dos ubicaciones:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-110">You can install UDF binaries in one of two locations:</span></span>
  
- <span data-ttu-id="c6d5e-111">Un directorio local.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-111">A local directory.</span></span> <span data-ttu-id="c6d5e-112">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-112">For example:</span></span> 
    
    <span data-ttu-id="c6d5e-113">C:\UDFs\MySampleUdf.dll</span><span class="sxs-lookup"><span data-stu-id="c6d5e-113">C:\UDFs\MySampleUdf.dll</span></span>
    
- <span data-ttu-id="c6d5e-114">La memoria caché de ensamblados global.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-114">The global assembly cache.</span></span> <span data-ttu-id="c6d5e-115">Por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-115">For example:</span></span> 
    
    <span data-ttu-id="c6d5e-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span><span class="sxs-lookup"><span data-stu-id="c6d5e-116">CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38</span></span>
    
<span data-ttu-id="c6d5e-117">Haga referencia a la ubicación cuando cree una definición **New-OfficeWebAppsExcelUserDefinedFunction** en Office Online Server.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-117">Reference the location when you create a **New-OfficeWebAppsExcelUserDefinedFunction** definition on the Office Online Server.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c6d5e-118">Office Online Server no admite las UDF que se encuentran en recursos compartidos de red.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-118">Office Online Server does not support UDFs located on network shares.</span></span> 
  
## <a name="enable-udfs-on-office-online-server"></a><span data-ttu-id="c6d5e-119">Habilitar UDF en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="c6d5e-119">Enable UDFs on Office Online Server</span></span> 

<span data-ttu-id="c6d5e-120">Cuando un administrador crea una nueva granja de servidores de Office Web Apps Server mediante el cmdlet de Windows PowerShell [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) , los ensamblados UDF están deshabilitados de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-120">When an adminstrator creates a new Office Web Apps Server farm by using the [New-OfficeWebAppsFarm](https://technet.microsoft.com/en-us/library/jj219436.aspx) Windows PowerShell cmdlet, UDF assemblies are disabled by default.</span></span> <span data-ttu-id="c6d5e-121">El valor predeterminado de la marca **ExcelUdfsAllowed** es false.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-121">The default value of the **ExcelUdfsAllowed** flag is false.</span></span> 
  
<span data-ttu-id="c6d5e-122">Para habilitar las UDF, ejecute el siguiente comando de Windows PowerShell en Office Online Server, una vez creada la granja de Office Web Apps Server.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-122">To enable UDFs, run the following Windows PowerShell command on the Office Online Server, after the Office Web Apps Server farm has been created.</span></span>
  
`Set-OfficeWebAppsFarm - ExcelUdfsAllowed:$true`
  
## <a name="create-udf-definitions-on-office-online-server"></a><span data-ttu-id="c6d5e-123">Crear definiciones de UDF en Office Online Server</span><span class="sxs-lookup"><span data-stu-id="c6d5e-123">Create UDF definitions on Office Online Server</span></span>

<span data-ttu-id="c6d5e-124">Después de habilitar las UDF, debe crear una definición para el binario que contiene las UDF.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-124">After you enable UDFs, you need to create a definition for the binary that contains the UDFs.</span></span> <span data-ttu-id="c6d5e-125">Para crear una definición para el binario de UDF en Office Online Server, use el cmdlet **New-OfficeWebAppsExcelUserDefinedFunction** .</span><span class="sxs-lookup"><span data-stu-id="c6d5e-125">To create a definition for your UDF binary on the Office Online Server, use the **New-OfficeWebAppsExcelUserDefinedFunction** cmdlet.</span></span> <span data-ttu-id="c6d5e-126">Este cmdlet incluye los siguientes parámetros:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-126">This cmdlet includes the following parameters:</span></span> 
  
- <span data-ttu-id="c6d5e-127">**MyAssembly**</span><span class="sxs-lookup"><span data-stu-id="c6d5e-127">**Assembly**</span></span>
    
- <span data-ttu-id="c6d5e-128">**AssemblyLocation**</span><span class="sxs-lookup"><span data-stu-id="c6d5e-128">**AssemblyLocation**</span></span>
    
- <span data-ttu-id="c6d5e-129">**Habilitar** (se establece en false de forma predeterminada)</span><span class="sxs-lookup"><span data-stu-id="c6d5e-129">**Enable** (set to False by default)</span></span> 
    
- <span data-ttu-id="c6d5e-130">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c6d5e-130">**Description**</span></span>
    
<span data-ttu-id="c6d5e-131">Los ejemplos siguientes muestran cómo crear las definiciones de UDF.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-131">The following examples show how create the UDF definitions.</span></span>
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly c:\myudf.dll -AssemblyLocation LocalFile -Enable:$true -Description "My Server UDFs"`
  
`New-OfficeWebAppsExcelUserDefinedFunction -Assembly "CompanyName.Hierarchichal.MyUdfNamespace.MyUdfClassName.dll, Version=1.1.0.0, Culture=en, PublicKeyToken=e8123117d7ba9ae38" -AssemblyLocation GAC -Enable:$true -Description "My GAC Server UDFs"`
  
<span data-ttu-id="c6d5e-132">Después de crear la nueva referencia de UDF, ejecute **iisreset** en el servidor para retomar la referencia inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-132">After you create the new UDF reference, run **iisreset** on the server to pick up the reference immediately.</span></span> 
  
## <a name="additional-office-online-server-udf-windows-powershell-commands"></a><span data-ttu-id="c6d5e-133">Otros comandos de Windows PowerShell de UDF de Office Online Server</span><span class="sxs-lookup"><span data-stu-id="c6d5e-133">Additional Office Online Server UDF Windows PowerShell commands</span></span>

<span data-ttu-id="c6d5e-134">Use los siguientes cmdlets de Windows PowerShell para trabajar con UDF:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-134">Use the following Windows PowerShell cmdlets to work with UDFs:</span></span>
  
- <span data-ttu-id="c6d5e-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (ningún parámetro obligatorio): devuelve una lista de las definiciones de UDF que están configuradas en el servidor de Office online.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-135">**Get-OfficeWebAppsExcelUserDefinedFunction** (no required parameters) - Returns a list of UDF definitions that are configured on the Office Online Server.</span></span> 
    
- <span data-ttu-id="c6d5e-136">**Set-OfficeWebAppsExcelUserDefinedFunction** (Parámetro Identity obligatorio): establece las propiedades de las definiciones UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-136">**Set- OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Sets properties on existing UDF definitions.</span></span> 
    
- <span data-ttu-id="c6d5e-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Parámetro Identity obligatorio): quita las definiciones UDF existentes.</span><span class="sxs-lookup"><span data-stu-id="c6d5e-137">**Remove-OfficeWebAppsExcelUserDefinedFunction** (Identity parameter required) - Removes existing UDF definitions.</span></span> 
    
## <a name="udf-sample"></a><span data-ttu-id="c6d5e-138">Ejemplo de UDF</span><span class="sxs-lookup"><span data-stu-id="c6d5e-138">UDF sample</span></span>

<span data-ttu-id="c6d5e-139">Los siguientes archivos proporcionan un libro de ejemplo que usa un archivo UDF y el binario UDF:</span><span class="sxs-lookup"><span data-stu-id="c6d5e-139">The following files provide a sample workbook that uses a UDF and the UDF binary:</span></span>
  
- <span data-ttu-id="c6d5e-140">[BooleanDataType. xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): un libro de ejemplo que usa un UDF</span><span class="sxs-lookup"><span data-stu-id="c6d5e-140">[BooleanDataType.xlsx](https://download.microsoft.com/download/6/7/F/67F724FD-1186-4209-BFF1-FBFD99E959D9/User%20Defined%20Function%20Assemblies/BooleanDataType.xlsx): a sample workbook that uses a UDF</span></span>  
- <span data-ttu-id="c6d5e-141">[EcsUdfsCommonSet. dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): el BINARIo UDF</span><span class="sxs-lookup"><span data-stu-id="c6d5e-141">[EcsUdfsCommonSet.dll](https://www.microsoft.com/en-us/search/result.aspx?q=EcsUdfsCommonSet.dll): the UDF binary</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c6d5e-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="c6d5e-142">See also</span></span>

- [<span data-ttu-id="c6d5e-143">Configurar las opciones administrativas de Excel Online</span><span class="sxs-lookup"><span data-stu-id="c6d5e-143">Configure Excel Online administrative settings</span></span>](https://docs.microsoft.com/officeonlineserver/configure-excel-online-administrative-settings)  
- [<span data-ttu-id="c6d5e-144">Office Online Server</span><span class="sxs-lookup"><span data-stu-id="c6d5e-144">Office Online Server</span></span>](https://docs.microsoft.com/officeonlineserver/office-online-server)
    

