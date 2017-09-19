## <a name="overview"></a><span data-ttu-id="1c0f0-101">概觀</span><span class="sxs-lookup"><span data-stu-id="1c0f0-101">Overview</span></span>

<span data-ttu-id="1c0f0-102">以下是您將建立的 API：</span><span class="sxs-lookup"><span data-stu-id="1c0f0-102">Here is the API that you’ll create:</span></span>

|<span data-ttu-id="1c0f0-103">API</span><span class="sxs-lookup"><span data-stu-id="1c0f0-103">API</span></span> | <span data-ttu-id="1c0f0-104">說明</span><span class="sxs-lookup"><span data-stu-id="1c0f0-104">Description</span></span>    | <span data-ttu-id="1c0f0-105">要求本文</span><span class="sxs-lookup"><span data-stu-id="1c0f0-105">Request body</span></span>    | <span data-ttu-id="1c0f0-106">回應本文</span><span class="sxs-lookup"><span data-stu-id="1c0f0-106">Response body</span></span>   |
|--- | ---- | ---- | ---- |
|<span data-ttu-id="1c0f0-107">GET /api/todo</span><span class="sxs-lookup"><span data-stu-id="1c0f0-107">GET /api/todo</span></span>  | <span data-ttu-id="1c0f0-108">取得所有待辦事項</span><span class="sxs-lookup"><span data-stu-id="1c0f0-108">Get all to-do items</span></span> | <span data-ttu-id="1c0f0-109">無</span><span class="sxs-lookup"><span data-stu-id="1c0f0-109">None</span></span> | <span data-ttu-id="1c0f0-110">待辦事項的陣列</span><span class="sxs-lookup"><span data-stu-id="1c0f0-110">Array of to-do items</span></span>|
|<span data-ttu-id="1c0f0-111">GET /api/todo/{id}</span><span class="sxs-lookup"><span data-stu-id="1c0f0-111">GET /api/todo/{id}</span></span>  | <span data-ttu-id="1c0f0-112">依識別碼取得項目</span><span class="sxs-lookup"><span data-stu-id="1c0f0-112">Get an item by ID</span></span> | <span data-ttu-id="1c0f0-113">無</span><span class="sxs-lookup"><span data-stu-id="1c0f0-113">None</span></span> | <span data-ttu-id="1c0f0-114">待辦事項</span><span class="sxs-lookup"><span data-stu-id="1c0f0-114">To-do item</span></span>|
|<span data-ttu-id="1c0f0-115">POST /api/todo</span><span class="sxs-lookup"><span data-stu-id="1c0f0-115">POST /api/todo</span></span> | <span data-ttu-id="1c0f0-116">新增記錄</span><span class="sxs-lookup"><span data-stu-id="1c0f0-116">Add a new item</span></span> | <span data-ttu-id="1c0f0-117">待辦事項</span><span class="sxs-lookup"><span data-stu-id="1c0f0-117">To-do item</span></span>  | <span data-ttu-id="1c0f0-118">待辦事項</span><span class="sxs-lookup"><span data-stu-id="1c0f0-118">To-do item</span></span> |
|<span data-ttu-id="1c0f0-119">PUT /api/todo/{id}</span><span class="sxs-lookup"><span data-stu-id="1c0f0-119">PUT /api/todo/{id}</span></span> | <span data-ttu-id="1c0f0-120">更新現有的項目 &nbsp;</span><span class="sxs-lookup"><span data-stu-id="1c0f0-120">Update an existing item &nbsp;</span></span>  | <span data-ttu-id="1c0f0-121">待辦事項</span><span class="sxs-lookup"><span data-stu-id="1c0f0-121">To-do item</span></span> |  <span data-ttu-id="1c0f0-122">無</span><span class="sxs-lookup"><span data-stu-id="1c0f0-122">None</span></span> |
|<span data-ttu-id="1c0f0-123">DELETE /api/todo/{id}  &nbsp;  &nbsp;</span><span class="sxs-lookup"><span data-stu-id="1c0f0-123">DELETE /api/todo/{id}  &nbsp;  &nbsp;</span></span> | <span data-ttu-id="1c0f0-124">刪除項目 &nbsp;  &nbsp;</span><span class="sxs-lookup"><span data-stu-id="1c0f0-124">Delete an item &nbsp;  &nbsp;</span></span>  | <span data-ttu-id="1c0f0-125">無</span><span class="sxs-lookup"><span data-stu-id="1c0f0-125">None</span></span>  | <span data-ttu-id="1c0f0-126">無</span><span class="sxs-lookup"><span data-stu-id="1c0f0-126">None</span></span>|

<br>

<span data-ttu-id="1c0f0-127">下圖顯示應用程式的基本設計。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-127">The following diagram shows the basic design of the app.</span></span>

![左側方塊所代表的用戶端會送出要求並接收來自應用程式 (右側繪製的方塊) 的回應。](../../tutorials/first-web-api/_static/architecture.png)

* <span data-ttu-id="1c0f0-132">用戶端是使用 Web API (行動裝置應用程式、瀏覽器等) 的任何項目。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-132">The client is whatever consumes the web API (mobile app, browser, etc).</span></span> <span data-ttu-id="1c0f0-133">我們不會在本教學課程中撰寫用戶端。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-133">We aren’t writing a client in this tutorial.</span></span> <span data-ttu-id="1c0f0-134">而是使用[Postman](https://www.getpostman.com/) 或 [curl](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/curl.1.html) 測試應用程式。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-134">We'll use [Postman](https://www.getpostman.com/) or [curl](https://developer.apple.com/legacy/library/documentation/Darwin/Reference/ManPages/man1/curl.1.html) to test the app.</span></span>

* <span data-ttu-id="1c0f0-135">「模型」是代表應用程式中資料的物件。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-135">A *model* is an object that represents the data in your application.</span></span> <span data-ttu-id="1c0f0-136">在此情況下，唯一的模型是待辦事項。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-136">In this case, the only model is a to-do item.</span></span> <span data-ttu-id="1c0f0-137">模型以 C# 類別表示，也稱純舊 C# 物件 (**P**lain **O**ld **C**# **O**bject, POCO)。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-137">Models are represented as C# classes, also know as **P**lain **O**ld **C**# **O**bject (POCOs).</span></span>

* <span data-ttu-id="1c0f0-138">「控制器」是用來處理 HTTP 要求並建立 HTTP 回應的物件。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-138">A *controller* is an object that handles HTTP requests and creates the HTTP response.</span></span> <span data-ttu-id="1c0f0-139">此應用程式將具有單一控制器。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-139">This app will have a single controller.</span></span>

* <span data-ttu-id="1c0f0-140">為了讓教學課程保持簡單，應用程式不會使用持續性資料庫。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-140">To keep the tutorial simple, the app doesn’t use a persistent database.</span></span> <span data-ttu-id="1c0f0-141">範例應用程式會在記憶體內部資料庫中儲存待辦事項。</span><span class="sxs-lookup"><span data-stu-id="1c0f0-141">The sample app stores to-do items in an in-memory database.</span></span>